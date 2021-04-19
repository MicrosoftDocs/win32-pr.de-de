---
description: Der Kryptografieanbieter von Microsoft ist der erste Kryptografiedienstanbieter-Anbieter (kryptografischen Service Provider, CSP) und wird mit den kryptoapi-Versionen 1,0 und 2,0 verteilt. Dabei handelt es sich um einen allgemeinen Anbieter, der digitale Signaturen und Datenverschlüsselung unterstützt.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Kryptografieanbieter von Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc48060305337dd878dedcadca8cfed52bd2f34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350466"
---
# <a name="microsoft-base-cryptographic-provider"></a><span data-ttu-id="88b57-104">Kryptografieanbieter von Microsoft</span><span class="sxs-lookup"><span data-stu-id="88b57-104">Microsoft Base Cryptographic Provider</span></span>

<span data-ttu-id="88b57-105">Der Kryptografieanbieter von Microsoft ist der erste [*Kryptografiedienstanbieter-Anbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) und wird mit den [*kryptoapi*](../secgloss/c-gly.md) -Versionen 1,0 und 2,0 verteilt.</span><span class="sxs-lookup"><span data-stu-id="88b57-105">The Microsoft Base Cryptographic Provider is the initial [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) provider, and is distributed with [*CryptoAPI*](../secgloss/c-gly.md) versions 1.0 and 2.0.</span></span> <span data-ttu-id="88b57-106">Dabei handelt es sich um einen allgemeinen Anbieter, der [*digitale Signaturen*](../secgloss/d-gly.md) und Datenverschlüsselung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88b57-106">It is a general-purpose provider that supports [*digital signatures*](../secgloss/d-gly.md) and data encryption.</span></span>

<span data-ttu-id="88b57-107">Der RSA-Algorithmus für öffentliche Schlüssel wird für alle Vorgänge mit öffentlichem Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="88b57-107">The RSA public key algorithm is used for all public key operations.</span></span>

<span data-ttu-id="88b57-108">Um die Abwärtskompatibilität mit früheren Versionen zu gewährleisten, behält die neue Version des Anbieters die Bezeichnung Version 1,0 des Namens in Wincrypt. h bei.</span><span class="sxs-lookup"><span data-stu-id="88b57-108">To maintain backward compatibility with earlier versions the new version of the provider retains the version 1.0 designation of the name in Wincrypt.h.</span></span> <span data-ttu-id="88b57-109">Die Version 2,0 dieses Anbieters wird jedoch zurzeit versendet.</span><span class="sxs-lookup"><span data-stu-id="88b57-109">However, version 2.0 of this provider is currently shipping.</span></span> <span data-ttu-id="88b57-110">Um die tatsächliche Version des verwendeten Anbieters zu ermitteln, nennen Sie [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) mit dem *dwparam* -Argument, das auf die **PP- \_ Version** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="88b57-110">To determine the actual version of the provider in use, call [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with the *dwParam* argument set to **PP\_VERSION**.</span></span> <span data-ttu-id="88b57-111">Wenn 0x0200 in *pbData* zurückgegeben wird, verfügen Sie über die Version 2,0.</span><span class="sxs-lookup"><span data-stu-id="88b57-111">If 0x0200 is returned in *pbData*, then you have version 2.0.</span></span>

|                |                     |
|----------------|---------------------|
| <span data-ttu-id="88b57-112">Anbietertyp:</span><span class="sxs-lookup"><span data-stu-id="88b57-112">Provider type:</span></span> | <span data-ttu-id="88b57-113">**Prov \_ RSA \_ Full**</span><span class="sxs-lookup"><span data-stu-id="88b57-113">**PROV\_RSA\_FULL**</span></span> |
| <span data-ttu-id="88b57-114">Anbieter Name:</span><span class="sxs-lookup"><span data-stu-id="88b57-114">Provider name:</span></span> | <span data-ttu-id="88b57-115">**MS \_ DEF \_ Prov**</span><span class="sxs-lookup"><span data-stu-id="88b57-115">**MS\_DEF\_PROV**</span></span>   |



 

 

 
