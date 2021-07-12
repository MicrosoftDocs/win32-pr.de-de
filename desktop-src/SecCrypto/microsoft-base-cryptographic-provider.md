---
description: Der Microsoft Base Cryptographic Provider ist der erste Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) und wird mit den CryptoAPI-Versionen 1.0 und 2.0 verteilt. Es ist ein allgemeiner Anbieter, der digitale Signaturen und Datenverschlüsselung unterstützt.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Microsoft Base Cryptographic Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53bd4b2f7faf140e57d25b54d3161b47dcaf740
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581888"
---
# <a name="microsoft-base-cryptographic-provider"></a><span data-ttu-id="9041b-104">Microsoft Base Cryptographic Provider</span><span class="sxs-lookup"><span data-stu-id="9041b-104">Microsoft Base Cryptographic Provider</span></span>

<span data-ttu-id="9041b-105">Der Microsoft Base Cryptographic Provider ist der erste Kryptografiedienstanbieter (Cryptographic [*Service Provider,*](../secgloss/c-gly.md) CSP) und wird mit [*den CryptoAPI-Versionen*](../secgloss/c-gly.md) 1.0 und 2.0 verteilt.</span><span class="sxs-lookup"><span data-stu-id="9041b-105">The Microsoft Base Cryptographic Provider is the initial [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) provider, and is distributed with [*CryptoAPI*](../secgloss/c-gly.md) versions 1.0 and 2.0.</span></span> <span data-ttu-id="9041b-106">Es ist ein allgemeiner Anbieter, der digitale [*Signaturen und*](../secgloss/d-gly.md) Datenverschlüsselung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9041b-106">It is a general-purpose provider that supports [*digital signatures*](../secgloss/d-gly.md) and data encryption.</span></span>

<span data-ttu-id="9041b-107">Der RSA-Algorithmus für öffentliche Schlüssel wird für alle Vorgänge mit öffentlichem Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="9041b-107">The RSA public key algorithm is used for all public key operations.</span></span>

<span data-ttu-id="9041b-108">Zur Aufrechterhaltung der Abwärtskompatibilität mit früheren Versionen behält die neue Version des Anbieters die Version 1.0-Bezeichnung des Namens in Wincrypt.h bei.</span><span class="sxs-lookup"><span data-stu-id="9041b-108">To maintain backward compatibility with earlier versions the new version of the provider retains the version 1.0 designation of the name in Wincrypt.h.</span></span> <span data-ttu-id="9041b-109">Version 2.0 dieses Anbieters wird derzeit jedoch im Versand verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="9041b-109">However, version 2.0 of this provider is currently shipping.</span></span> <span data-ttu-id="9041b-110">Um die tatsächliche Version des zu verwendenden Anbieters zu ermitteln, rufen Sie [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) auf, und legen Sie dabei das *argument dwParam* auf **PP VERSION \_ fest.**</span><span class="sxs-lookup"><span data-stu-id="9041b-110">To determine the actual version of the provider in use, call [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with the *dwParam* argument set to **PP\_VERSION**.</span></span> <span data-ttu-id="9041b-111">Wenn 0x0200 in *pbData* zurückgegeben wird, verfügen Sie über Version 2.0.</span><span class="sxs-lookup"><span data-stu-id="9041b-111">If 0x0200 is returned in *pbData*, then you have version 2.0.</span></span>

|                   | <span data-ttu-id="9041b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="9041b-112">Value</span></span>            |
|-------------------|------------------|
| <span data-ttu-id="9041b-113">**Anbietertyp**</span><span class="sxs-lookup"><span data-stu-id="9041b-113">**Provider type**</span></span> | <span data-ttu-id="9041b-114">PROV \_ RSA \_ FULL</span><span class="sxs-lookup"><span data-stu-id="9041b-114">PROV\_RSA\_FULL</span></span>  |
| <span data-ttu-id="9041b-115">**Anbietername**</span><span class="sxs-lookup"><span data-stu-id="9041b-115">**Provider name**</span></span> | <span data-ttu-id="9041b-116">MS \_ DEF \_ PROV</span><span class="sxs-lookup"><span data-stu-id="9041b-116">MS\_DEF\_PROV</span></span>    |



 

 

 
