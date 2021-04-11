---
description: Die Informationen in diesem Thema gelten für Windows Server 2003 und Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: Secure Sockets Layer-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed2555c854a6cc25948abe0dc83043ee632170
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959634"
---
# <a name="secure-sockets-layer-protocol"></a><span data-ttu-id="72a8a-103">Secure Sockets Layer-Protokoll</span><span class="sxs-lookup"><span data-stu-id="72a8a-103">Secure Sockets Layer Protocol</span></span>

<span data-ttu-id="72a8a-104">Die Informationen in diesem Thema gelten für Windows Server 2003 und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="72a8a-104">The information in this topic applies to Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="72a8a-105">Informationen zu Verschlüsselungs Sammlungen für Windows Server 2008 und Windows Vista finden Sie unter Verschlüsselungs Sammlungen [in Schannel](cipher-suites-in-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="72a8a-105">For cipher suites for Windows Server 2008 and Windows Vista, see [Cipher Suites in Schannel](cipher-suites-in-schannel.md).</span></span>

<span data-ttu-id="72a8a-106">SChannel unterstützt die Versionen 2,0 und 3,0 des [*Secure Sockets Layer (SSL)-Protokolls*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="72a8a-106">Schannel supports versions 2.0 and 3.0 of the [*Secure Sockets Layer (SSL) protocol*](../secgloss/s-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="72a8a-107">Ab Windows 10, Version 1607 und Windows Server 2016, wurde SSL 2,0 entfernt und wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="72a8a-107">Beginning with Windows 10, version 1607 and Windows Server 2016, SSL 2.0 has been removed and is no longer supported.</span></span>

 

## <a name="ssl-30"></a><span data-ttu-id="72a8a-108">SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="72a8a-108">SSL 3.0</span></span>

<span data-ttu-id="72a8a-109">SSL 3,0 ist der Vorgänger des [Transport Layer Security Protokolls](transport-layer-security-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="72a8a-109">SSL 3.0 is the predecessor of the [Transport Layer Security Protocol](transport-layer-security-protocol.md).</span></span>

<span data-ttu-id="72a8a-110">SChannel unterstützt die Verschlüsselungs Sammlungen, die unter [TLS Chiffre Suites](tls-cipher-suites.md) for SSL 3,0 aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="72a8a-110">Schannel supports the cipher suites listed under [TLS Cipher Suites](tls-cipher-suites.md) for SSL 3.0.</span></span> <span data-ttu-id="72a8a-111">SSL 3,0 unterstützt alle Verschlüsselungs Sammlungen, die unter TLS-Verschlüsselungs Sammlungen aufgeführt sind, sowie SSL- \_ Fortezza \_ KEA \_ mit \_ Fortezza \_ CBC \_ SHA.</span><span class="sxs-lookup"><span data-stu-id="72a8a-111">SSL 3.0 supports all of the cipher suites listed under TLS Cipher Suites as well as SSL\_FORTEZZA\_KEA\_WITH\_FORTEZZA\_CBC\_SHA.</span></span>

## <a name="ssl-20"></a><span data-ttu-id="72a8a-112">SSL 2.0</span><span class="sxs-lookup"><span data-stu-id="72a8a-112">SSL 2.0</span></span>

<span data-ttu-id="72a8a-113">SSL 2,0 wurde durch TLS abgelöst und sollte nicht für die neue Entwicklung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72a8a-113">SSL 2.0 has been superseded by TLS and should not be used for new development.</span></span>

<span data-ttu-id="72a8a-114">SChannel unterstützt die folgenden Verschlüsselungs Sammlungen für SSL 2,0.</span><span class="sxs-lookup"><span data-stu-id="72a8a-114">Schannel supports the following cipher suites for SSL 2.0.</span></span> <span data-ttu-id="72a8a-115">Die Auflistungen werden in der Reihenfolge von den sichersten bis zum geringsten sicher aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="72a8a-115">The suites are listed in order from most secure to least secure.</span></span>

-   <span data-ttu-id="72a8a-116">SSL \_ RC4 \_ 128 \_ mit \_ MD5</span><span class="sxs-lookup"><span data-stu-id="72a8a-116">SSL\_RC4\_128\_WITH\_MD5</span></span>
-   <span data-ttu-id="72a8a-117">SSL \_ des \_ 192 \_ EDE3 \_ CBC \_ mit \_ MD5</span><span class="sxs-lookup"><span data-stu-id="72a8a-117">SSL\_DES\_192\_EDE3\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="72a8a-118">SSL \_ RC2 \_ CBC \_ 128 \_ CBC \_ mit \_ MD5</span><span class="sxs-lookup"><span data-stu-id="72a8a-118">SSL\_RC2\_CBC\_128\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="72a8a-119">SSL \_ des \_ 64 \_ CBC \_ mit \_ MD5</span><span class="sxs-lookup"><span data-stu-id="72a8a-119">SSL\_DES\_64\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="72a8a-120">SSL \_ RC4 \_ 128 \_ EXPORT40 \_ mit \_ MD5</span><span class="sxs-lookup"><span data-stu-id="72a8a-120">SSL\_RC4\_128\_EXPORT40\_WITH\_MD5</span></span>

 

 
