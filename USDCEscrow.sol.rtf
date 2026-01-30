{\rtf1\ansi\ansicpg1252\cocoartf2761
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fnil\fcharset0 Menlo-Regular;}
{\colortbl;\red255\green255\blue255;\red79\green123\blue61;\red191\green80\blue83;\red145\green145\blue175;
\red70\green137\blue204;\red212\green212\blue212;\red167\green197\blue152;\red194\green126\blue101;\red238\green138\blue18;
\red23\green178\blue121;\red117\green117\blue117;\red223\green33\blue121;\red42\green71\blue108;\red43\green132\blue210;
\red140\green108\blue11;}
{\*\expandedcolortbl;;\cssrgb\c37647\c54510\c30588;\cssrgb\c80000\c40000\c40000;\cssrgb\c63529\c63922\c74118;
\cssrgb\c33725\c61176\c83922;\cssrgb\c86275\c86275\c86275;\cssrgb\c70980\c80784\c65882;\cssrgb\c80784\c56863\c47059;\cssrgb\c95294\c61176\c7059;
\cssrgb\c0\c73725\c54902;\cssrgb\c53333\c53333\c53333;\cssrgb\c90980\c24314\c54902;\cssrgb\c21569\c35294\c49804;\cssrgb\c20392\c59608\c85882;
\cssrgb\c61961\c49412\c3137;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\deftab720
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf2 \cb3 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 // SPDX-License-Identifier: MIT\cf4 \cb1 \strokec4 \
\pard\pardeftab720\partightenfactor0
\cf5 \cb3 \strokec5 pragma\cf4 \strokec4  \cf5 \strokec5 solidity\cf4 \strokec4  \cf6 \strokec6 ^\cf7 \strokec7 0.8.19\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\
\cf5 \cb3 \strokec5 import\cf4 \strokec4  \cf8 \strokec8 "@openzeppelin/contracts/token/ERC20/IERC20.sol"\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cf5 \cb3 \strokec5 import\cf4 \strokec4  \cf8 \strokec8 "@openzeppelin/contracts/token/ERC20/utils/SafeERC20.sol"\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cf5 \cb3 \strokec5 import\cf4 \strokec4  \cf8 \strokec8 "@openzeppelin/contracts/security/ReentrancyGuard.sol"\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\
\pard\pardeftab720\partightenfactor0
\cf2 \cb3 \strokec2 /**\cf4 \cb1 \strokec4 \
\cf2 \cb3 \strokec2  * @title USDCEscrow\cf4 \cb1 \strokec4 \
\cf2 \cb3 \strokec2  * @notice A simple escrow contract for USDC on Arc Testnet\cf4 \cb1 \strokec4 \
\cf2 \cb3 \strokec2  * @dev Requires mutual agreement or timeout for fund release\cf4 \cb1 \strokec4 \
\cf2 \cb3 \strokec2  */\cf4 \cb1 \strokec4 \
\pard\pardeftab720\partightenfactor0
\cf5 \cb3 \strokec5 contract\cf4 \strokec4  USDCEscrow \cf5 \strokec5 is\cf4 \strokec4  ReentrancyGuard \cf6 \strokec6 \{\cf4 \cb1 \strokec4 \
\pard\pardeftab720\partightenfactor0
\cf4 \cb3     \cf5 \strokec5 using\cf4 \strokec4  SafeERC20 \cf9 \strokec9 for\cf4 \strokec4  IERC20\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\
\cb3     \cf2 \strokec2 // USDC token address on Arc Testnet (also used for gas)\cf4 \cb1 \strokec4 \
\cb3     IERC20 \cf10 \strokec10 public\cf4 \strokec4  \cf11 \strokec11 immutable\cf4 \strokec4  usdc\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\
\cb3     \cf5 \strokec5 struct\cf4 \strokec4  Escrow \cf6 \strokec6 \{\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 address\cf4 \strokec4  sender\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 address\cf4 \strokec4  receiver\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 uint256\cf4 \strokec4  amount\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 uint256\cf4 \strokec4  deadline\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 bool\cf4 \strokec4  senderApproved\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 bool\cf4 \strokec4  receiverApproved\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 bool\cf4 \strokec4  completed\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 bool\cf4 \strokec4  refunded\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cb3     \cf6 \strokec6 \}\cf4 \cb1 \strokec4 \
\
\cb3     \cf5 \strokec5 uint256\cf4 \strokec4  \cf10 \strokec10 public\cf4 \strokec4  escrowCounter\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cb3     \cf5 \strokec5 mapping\cf6 \strokec6 (\cf5 \strokec5 uint256\cf4 \strokec4  => Escrow\cf6 \strokec6 )\cf4 \strokec4  \cf10 \strokec10 public\cf4 \strokec4  escrows\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\
\cb3     \cf5 \strokec5 event\cf4 \strokec4  EscrowCreated\cf6 \strokec6 (\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 uint256\cf4 \strokec4  \cf9 \strokec9 indexed\cf4 \strokec4  escrowId\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 address\cf4 \strokec4  \cf9 \strokec9 indexed\cf4 \strokec4  sender\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 address\cf4 \strokec4  \cf9 \strokec9 indexed\cf4 \strokec4  receiver\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 uint256\cf4 \strokec4  amount\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 uint256\cf4 \strokec4  deadline\cb1 \
\cb3     \cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3     \cf5 \strokec5 event\cf4 \strokec4  Approved\cf6 \strokec6 (\cf5 \strokec5 uint256\cf4 \strokec4  \cf9 \strokec9 indexed\cf4 \strokec4  escrowId\cf6 \strokec6 ,\cf4 \strokec4  \cf5 \strokec5 address\cf4 \strokec4  \cf9 \strokec9 indexed\cf4 \strokec4  approver\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3     \cf5 \strokec5 event\cf4 \strokec4  FundsReleased\cf6 \strokec6 (\cf5 \strokec5 uint256\cf4 \strokec4  \cf9 \strokec9 indexed\cf4 \strokec4  escrowId\cf6 \strokec6 ,\cf4 \strokec4  \cf5 \strokec5 address\cf4 \strokec4  \cf9 \strokec9 indexed\cf4 \strokec4  receiver\cf6 \strokec6 ,\cf4 \strokec4  \cf5 \strokec5 uint256\cf4 \strokec4  amount\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3     \cf5 \strokec5 event\cf4 \strokec4  FundsRefunded\cf6 \strokec6 (\cf5 \strokec5 uint256\cf4 \strokec4  \cf9 \strokec9 indexed\cf4 \strokec4  escrowId\cf6 \strokec6 ,\cf4 \strokec4  \cf5 \strokec5 address\cf4 \strokec4  \cf9 \strokec9 indexed\cf4 \strokec4  sender\cf6 \strokec6 ,\cf4 \strokec4  \cf5 \strokec5 uint256\cf4 \strokec4  amount\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\
\cb3     \cf12 \strokec12 constructor\cf6 \strokec6 (\cf5 \strokec5 address\cf4 \strokec4  _usdcAddress\cf6 \strokec6 )\cf4 \strokec4  \cf6 \strokec6 \{\cf4 \cb1 \strokec4 \
\cb3         \cf13 \strokec13 require\cf6 \strokec6 (\cf4 \strokec4 _usdcAddress \cf6 \strokec6 !=\cf4 \strokec4  \cf5 \strokec5 address\cf6 \strokec6 (\cf7 \strokec7 0\cf6 \strokec6 ),\cf4 \strokec4  \cf8 \strokec8 "Invalid USDC address"\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3         usdc \cf6 \strokec6 =\cf4 \strokec4  IERC20\cf6 \strokec6 (\cf4 \strokec4 _usdcAddress\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3     \cf6 \strokec6 \}\cf4 \cb1 \strokec4 \
\
\cb3     \cf2 \strokec2 /**\cf4 \cb1 \strokec4 \
\pard\pardeftab720\partightenfactor0
\cf2 \cb3 \strokec2      * @notice Create a new escrow\cf4 \cb1 \strokec4 \
\cf2 \cb3 \strokec2      * @param _receiver Address that will receive funds upon agreement\cf4 \cb1 \strokec4 \
\cf2 \cb3 \strokec2      * @param _amount Amount of USDC to escrow\cf4 \cb1 \strokec4 \
\cf2 \cb3 \strokec2      * @param _duration Time in seconds until auto-refund is possible\cf4 \cb1 \strokec4 \
\cf2 \cb3 \strokec2      */\cf4 \cb1 \strokec4 \
\pard\pardeftab720\partightenfactor0
\cf4 \cb3     \cf5 \strokec5 function\cf4 \strokec4  createEscrow\cf6 \strokec6 (\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 address\cf4 \strokec4  _receiver\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 uint256\cf4 \strokec4  _amount\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 uint256\cf4 \strokec4  _duration\cb1 \
\cb3     \cf6 \strokec6 )\cf4 \strokec4  \cf10 \strokec10 external\cf4 \strokec4  nonReentrant \cf10 \strokec10 returns\cf4 \strokec4  \cf6 \strokec6 (\cf5 \strokec5 uint256\cf6 \strokec6 )\cf4 \strokec4  \cf6 \strokec6 \{\cf4 \cb1 \strokec4 \
\cb3         \cf13 \strokec13 require\cf6 \strokec6 (\cf4 \strokec4 _receiver \cf6 \strokec6 !=\cf4 \strokec4  \cf5 \strokec5 address\cf6 \strokec6 (\cf7 \strokec7 0\cf6 \strokec6 ),\cf4 \strokec4  \cf8 \strokec8 "Invalid receiver"\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3         \cf13 \strokec13 require\cf6 \strokec6 (\cf4 \strokec4 _receiver \cf6 \strokec6 !=\cf4 \strokec4  \cf13 \strokec13 msg\cf6 \strokec6 .\cf4 \strokec4 sender\cf6 \strokec6 ,\cf4 \strokec4  \cf8 \strokec8 "Cannot escrow to yourself"\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3         \cf13 \strokec13 require\cf6 \strokec6 (\cf4 \strokec4 _amount \cf6 \strokec6 >\cf4 \strokec4  \cf7 \strokec7 0\cf6 \strokec6 ,\cf4 \strokec4  \cf8 \strokec8 "Amount must be > 0"\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3         \cf13 \strokec13 require\cf6 \strokec6 (\cf4 \strokec4 _duration \cf6 \strokec6 >=\cf4 \strokec4  \cf7 \strokec7 1\cf4 \strokec4  hours\cf6 \strokec6 ,\cf4 \strokec4  \cf8 \strokec8 "Duration must be >= 1 hour"\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3         \cf13 \strokec13 require\cf6 \strokec6 (\cf4 \strokec4 _duration \cf6 \strokec6 <=\cf4 \strokec4  \cf7 \strokec7 30\cf4 \strokec4  days\cf6 \strokec6 ,\cf4 \strokec4  \cf8 \strokec8 "Duration must be <= 30 days"\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\
\cb3         \cf2 \strokec2 // Transfer USDC from sender to contract\cf4 \cb1 \strokec4 \
\cb3         usdc\cf6 \strokec6 .\cf4 \strokec4 safeTransferFrom\cf6 \strokec6 (\cf13 \strokec13 msg\cf6 \strokec6 .\cf4 \strokec4 sender\cf6 \strokec6 ,\cf4 \strokec4  \cf5 \strokec5 address\cf6 \strokec6 (\cf14 \strokec14 this\cf6 \strokec6 ),\cf4 \strokec4  _amount\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\
\cb3         \cf5 \strokec5 uint256\cf4 \strokec4  escrowId \cf6 \strokec6 =\cf4 \strokec4  escrowCounter\cf6 \strokec6 ++;\cf4 \cb1 \strokec4 \
\cb3         escrows\cf6 \strokec6 [\cf4 \strokec4 escrowId\cf6 \strokec6 ]\cf4 \strokec4  \cf6 \strokec6 =\cf4 \strokec4  Escrow\cf6 \strokec6 (\{\cf4 \cb1 \strokec4 \
\cb3             sender\cf6 \strokec6 :\cf4 \strokec4  \cf13 \strokec13 msg\cf6 \strokec6 .\cf4 \strokec4 sender\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3             receiver\cf6 \strokec6 :\cf4 \strokec4  _receiver\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3             amount\cf6 \strokec6 :\cf4 \strokec4  _amount\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3             deadline\cf6 \strokec6 :\cf4 \strokec4  \cf13 \strokec13 block\cf6 \strokec6 .\cf4 \strokec4 timestamp \cf6 \strokec6 +\cf4 \strokec4  _duration\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3             senderApproved\cf6 \strokec6 :\cf4 \strokec4  \cf5 \strokec5 false\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3             receiverApproved\cf6 \strokec6 :\cf4 \strokec4  \cf5 \strokec5 false\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3             completed\cf6 \strokec6 :\cf4 \strokec4  \cf5 \strokec5 false\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3             refunded\cf6 \strokec6 :\cf4 \strokec4  \cf5 \strokec5 false\cf4 \cb1 \strokec4 \
\cb3         \cf6 \strokec6 \});\cf4 \cb1 \strokec4 \
\
\cb3         \cf5 \strokec5 emit\cf4 \strokec4  EscrowCreated\cf6 \strokec6 (\cf4 \strokec4 escrowId\cf6 \strokec6 ,\cf4 \strokec4  \cf13 \strokec13 msg\cf6 \strokec6 .\cf4 \strokec4 sender\cf6 \strokec6 ,\cf4 \strokec4  _receiver\cf6 \strokec6 ,\cf4 \strokec4  _amount\cf6 \strokec6 ,\cf4 \strokec4  \cf13 \strokec13 block\cf6 \strokec6 .\cf4 \strokec4 timestamp \cf6 \strokec6 +\cf4 \strokec4  _duration\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3         \cf10 \strokec10 return\cf4 \strokec4  escrowId\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cb3     \cf6 \strokec6 \}\cf4 \cb1 \strokec4 \
\
\cb3     \cf2 \strokec2 /**\cf4 \cb1 \strokec4 \
\pard\pardeftab720\partightenfactor0
\cf2 \cb3 \strokec2      * @notice Approve the release of funds\cf4 \cb1 \strokec4 \
\cf2 \cb3 \strokec2      * @param _escrowId The escrow to approve\cf4 \cb1 \strokec4 \
\cf2 \cb3 \strokec2      */\cf4 \cb1 \strokec4 \
\pard\pardeftab720\partightenfactor0
\cf4 \cb3     \cf5 \strokec5 function\cf4 \strokec4  approve\cf6 \strokec6 (\cf5 \strokec5 uint256\cf4 \strokec4  _escrowId\cf6 \strokec6 )\cf4 \strokec4  \cf10 \strokec10 external\cf4 \strokec4  nonReentrant \cf6 \strokec6 \{\cf4 \cb1 \strokec4 \
\cb3         Escrow \cf15 \strokec15 storage\cf4 \strokec4  escrow \cf6 \strokec6 =\cf4 \strokec4  escrows\cf6 \strokec6 [\cf4 \strokec4 _escrowId\cf6 \strokec6 ];\cf4 \cb1 \strokec4 \
\cb3         \cf13 \strokec13 require\cf6 \strokec6 (!\cf4 \strokec4 escrow\cf6 \strokec6 .\cf4 \strokec4 completed \cf6 \strokec6 &&\cf4 \strokec4  \cf6 \strokec6 !\cf4 \strokec4 escrow\cf6 \strokec6 .\cf4 \strokec4 refunded\cf6 \strokec6 ,\cf4 \strokec4  \cf8 \strokec8 "Escrow already finalized"\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3         \cf13 \strokec13 require\cf6 \strokec6 (\cf4 \cb1 \strokec4 \
\cb3             \cf13 \strokec13 msg\cf6 \strokec6 .\cf4 \strokec4 sender \cf6 \strokec6 ==\cf4 \strokec4  escrow\cf6 \strokec6 .\cf4 \strokec4 sender \cf6 \strokec6 ||\cf4 \strokec4  \cf13 \strokec13 msg\cf6 \strokec6 .\cf4 \strokec4 sender \cf6 \strokec6 ==\cf4 \strokec4  escrow\cf6 \strokec6 .\cf4 \strokec4 receiver\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3             \cf8 \strokec8 "Not a party to this escrow"\cf4 \cb1 \strokec4 \
\cb3         \cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\
\cb3         \cf9 \strokec9 if\cf4 \strokec4  \cf6 \strokec6 (\cf13 \strokec13 msg\cf6 \strokec6 .\cf4 \strokec4 sender \cf6 \strokec6 ==\cf4 \strokec4  escrow\cf6 \strokec6 .\cf4 \strokec4 sender\cf6 \strokec6 )\cf4 \strokec4  \cf6 \strokec6 \{\cf4 \cb1 \strokec4 \
\cb3             \cf13 \strokec13 require\cf6 \strokec6 (!\cf4 \strokec4 escrow\cf6 \strokec6 .\cf4 \strokec4 senderApproved\cf6 \strokec6 ,\cf4 \strokec4  \cf8 \strokec8 "Already approved"\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3             escrow\cf6 \strokec6 .\cf4 \strokec4 senderApproved \cf6 \strokec6 =\cf4 \strokec4  \cf5 \strokec5 true\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cb3         \cf6 \strokec6 \}\cf4 \strokec4  \cf9 \strokec9 else\cf4 \strokec4  \cf6 \strokec6 \{\cf4 \cb1 \strokec4 \
\cb3             \cf13 \strokec13 require\cf6 \strokec6 (!\cf4 \strokec4 escrow\cf6 \strokec6 .\cf4 \strokec4 receiverApproved\cf6 \strokec6 ,\cf4 \strokec4  \cf8 \strokec8 "Already approved"\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3             escrow\cf6 \strokec6 .\cf4 \strokec4 receiverApproved \cf6 \strokec6 =\cf4 \strokec4  \cf5 \strokec5 true\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cb3         \cf6 \strokec6 \}\cf4 \cb1 \strokec4 \
\
\cb3         \cf5 \strokec5 emit\cf4 \strokec4  Approved\cf6 \strokec6 (\cf4 \strokec4 _escrowId\cf6 \strokec6 ,\cf4 \strokec4  \cf13 \strokec13 msg\cf6 \strokec6 .\cf4 \strokec4 sender\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\
\cb3         \cf2 \strokec2 // If both parties approved, release funds\cf4 \cb1 \strokec4 \
\cb3         \cf9 \strokec9 if\cf4 \strokec4  \cf6 \strokec6 (\cf4 \strokec4 escrow\cf6 \strokec6 .\cf4 \strokec4 senderApproved \cf6 \strokec6 &&\cf4 \strokec4  escrow\cf6 \strokec6 .\cf4 \strokec4 receiverApproved\cf6 \strokec6 )\cf4 \strokec4  \cf6 \strokec6 \{\cf4 \cb1 \strokec4 \
\cb3             _releaseFunds\cf6 \strokec6 (\cf4 \strokec4 _escrowId\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3         \cf6 \strokec6 \}\cf4 \cb1 \strokec4 \
\cb3     \cf6 \strokec6 \}\cf4 \cb1 \strokec4 \
\
\cb3     \cf2 \strokec2 /**\cf4 \cb1 \strokec4 \
\pard\pardeftab720\partightenfactor0
\cf2 \cb3 \strokec2      * @notice Claim refund after deadline (only sender)\cf4 \cb1 \strokec4 \
\cf2 \cb3 \strokec2      * @param _escrowId The escrow to refund\cf4 \cb1 \strokec4 \
\cf2 \cb3 \strokec2      */\cf4 \cb1 \strokec4 \
\pard\pardeftab720\partightenfactor0
\cf4 \cb3     \cf5 \strokec5 function\cf4 \strokec4  claimRefund\cf6 \strokec6 (\cf5 \strokec5 uint256\cf4 \strokec4  _escrowId\cf6 \strokec6 )\cf4 \strokec4  \cf10 \strokec10 external\cf4 \strokec4  nonReentrant \cf6 \strokec6 \{\cf4 \cb1 \strokec4 \
\cb3         Escrow \cf15 \strokec15 storage\cf4 \strokec4  escrow \cf6 \strokec6 =\cf4 \strokec4  escrows\cf6 \strokec6 [\cf4 \strokec4 _escrowId\cf6 \strokec6 ];\cf4 \cb1 \strokec4 \
\cb3         \cf13 \strokec13 require\cf6 \strokec6 (!\cf4 \strokec4 escrow\cf6 \strokec6 .\cf4 \strokec4 completed \cf6 \strokec6 &&\cf4 \strokec4  \cf6 \strokec6 !\cf4 \strokec4 escrow\cf6 \strokec6 .\cf4 \strokec4 refunded\cf6 \strokec6 ,\cf4 \strokec4  \cf8 \strokec8 "Escrow already finalized"\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3         \cf13 \strokec13 require\cf6 \strokec6 (\cf13 \strokec13 msg\cf6 \strokec6 .\cf4 \strokec4 sender \cf6 \strokec6 ==\cf4 \strokec4  escrow\cf6 \strokec6 .\cf4 \strokec4 sender\cf6 \strokec6 ,\cf4 \strokec4  \cf8 \strokec8 "Only sender can claim refund"\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3         \cf13 \strokec13 require\cf6 \strokec6 (\cf13 \strokec13 block\cf6 \strokec6 .\cf4 \strokec4 timestamp \cf6 \strokec6 >=\cf4 \strokec4  escrow\cf6 \strokec6 .\cf4 \strokec4 deadline\cf6 \strokec6 ,\cf4 \strokec4  \cf8 \strokec8 "Deadline not reached"\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\
\cb3         escrow\cf6 \strokec6 .\cf4 \strokec4 refunded \cf6 \strokec6 =\cf4 \strokec4  \cf5 \strokec5 true\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cb3         usdc\cf6 \strokec6 .\cf4 \strokec4 safeTransfer\cf6 \strokec6 (\cf4 \strokec4 escrow\cf6 \strokec6 .\cf4 \strokec4 sender\cf6 \strokec6 ,\cf4 \strokec4  escrow\cf6 \strokec6 .\cf4 \strokec4 amount\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\
\cb3         \cf5 \strokec5 emit\cf4 \strokec4  FundsRefunded\cf6 \strokec6 (\cf4 \strokec4 _escrowId\cf6 \strokec6 ,\cf4 \strokec4  escrow\cf6 \strokec6 .\cf4 \strokec4 sender\cf6 \strokec6 ,\cf4 \strokec4  escrow\cf6 \strokec6 .\cf4 \strokec4 amount\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3     \cf6 \strokec6 \}\cf4 \cb1 \strokec4 \
\
\cb3     \cf2 \strokec2 /**\cf4 \cb1 \strokec4 \
\pard\pardeftab720\partightenfactor0
\cf2 \cb3 \strokec2      * @notice Internal function to release funds to receiver\cf4 \cb1 \strokec4 \
\cf2 \cb3 \strokec2      */\cf4 \cb1 \strokec4 \
\pard\pardeftab720\partightenfactor0
\cf4 \cb3     \cf5 \strokec5 function\cf4 \strokec4  _releaseFunds\cf6 \strokec6 (\cf5 \strokec5 uint256\cf4 \strokec4  _escrowId\cf6 \strokec6 )\cf4 \strokec4  \cf10 \strokec10 internal\cf4 \strokec4  \cf6 \strokec6 \{\cf4 \cb1 \strokec4 \
\cb3         Escrow \cf15 \strokec15 storage\cf4 \strokec4  escrow \cf6 \strokec6 =\cf4 \strokec4  escrows\cf6 \strokec6 [\cf4 \strokec4 _escrowId\cf6 \strokec6 ];\cf4 \cb1 \strokec4 \
\cb3         escrow\cf6 \strokec6 .\cf4 \strokec4 completed \cf6 \strokec6 =\cf4 \strokec4  \cf5 \strokec5 true\cf6 \strokec6 ;\cf4 \cb1 \strokec4 \
\cb3         usdc\cf6 \strokec6 .\cf4 \strokec4 safeTransfer\cf6 \strokec6 (\cf4 \strokec4 escrow\cf6 \strokec6 .\cf4 \strokec4 receiver\cf6 \strokec6 ,\cf4 \strokec4  escrow\cf6 \strokec6 .\cf4 \strokec4 amount\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\
\cb3         \cf5 \strokec5 emit\cf4 \strokec4  FundsReleased\cf6 \strokec6 (\cf4 \strokec4 _escrowId\cf6 \strokec6 ,\cf4 \strokec4  escrow\cf6 \strokec6 .\cf4 \strokec4 receiver\cf6 \strokec6 ,\cf4 \strokec4  escrow\cf6 \strokec6 .\cf4 \strokec4 amount\cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3     \cf6 \strokec6 \}\cf4 \cb1 \strokec4 \
\
\cb3     \cf2 \strokec2 /**\cf4 \cb1 \strokec4 \
\pard\pardeftab720\partightenfactor0
\cf2 \cb3 \strokec2      * @notice Get escrow details\cf4 \cb1 \strokec4 \
\cf2 \cb3 \strokec2      */\cf4 \cb1 \strokec4 \
\pard\pardeftab720\partightenfactor0
\cf4 \cb3     \cf5 \strokec5 function\cf4 \strokec4  getEscrow\cf6 \strokec6 (\cf5 \strokec5 uint256\cf4 \strokec4  _escrowId\cf6 \strokec6 )\cf4 \strokec4  \cf10 \strokec10 external\cf4 \strokec4  \cf10 \strokec10 view\cf4 \strokec4  \cf10 \strokec10 returns\cf4 \strokec4  \cf6 \strokec6 (\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 address\cf4 \strokec4  sender\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 address\cf4 \strokec4  receiver\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 uint256\cf4 \strokec4  amount\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 uint256\cf4 \strokec4  deadline\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 bool\cf4 \strokec4  senderApproved\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 bool\cf4 \strokec4  receiverApproved\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 bool\cf4 \strokec4  completed\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3         \cf5 \strokec5 bool\cf4 \strokec4  refunded\cb1 \
\cb3     \cf6 \strokec6 )\cf4 \strokec4  \cf6 \strokec6 \{\cf4 \cb1 \strokec4 \
\cb3         Escrow \cf15 \strokec15 storage\cf4 \strokec4  e \cf6 \strokec6 =\cf4 \strokec4  escrows\cf6 \strokec6 [\cf4 \strokec4 _escrowId\cf6 \strokec6 ];\cf4 \cb1 \strokec4 \
\cb3         \cf10 \strokec10 return\cf4 \strokec4  \cf6 \strokec6 (\cf4 \cb1 \strokec4 \
\cb3             e\cf6 \strokec6 .\cf4 \strokec4 sender\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3             e\cf6 \strokec6 .\cf4 \strokec4 receiver\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3             e\cf6 \strokec6 .\cf4 \strokec4 amount\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3             e\cf6 \strokec6 .\cf4 \strokec4 deadline\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3             e\cf6 \strokec6 .\cf4 \strokec4 senderApproved\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3             e\cf6 \strokec6 .\cf4 \strokec4 receiverApproved\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3             e\cf6 \strokec6 .\cf4 \strokec4 completed\cf6 \strokec6 ,\cf4 \cb1 \strokec4 \
\cb3             e\cf6 \strokec6 .\cf4 \strokec4 refunded\cb1 \
\cb3         \cf6 \strokec6 );\cf4 \cb1 \strokec4 \
\cb3     \cf6 \strokec6 \}\cf4 \cb1 \strokec4 \
\pard\pardeftab720\partightenfactor0
\cf6 \cb3 \strokec6 \}\cf4 \cb1 \strokec4 \
}