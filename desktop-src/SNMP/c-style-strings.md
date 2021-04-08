---
title: Zeichen folgen im C-Stil
description: Eine WinSNMP-Anwendung kann mit NULL endende Zeichen folgen im C-Stil zum Konvertieren von Entitäts-und objektbezeichnerobjekten (OID) in und aus ihren Zeichen folgen Darstellungen verwenden.
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878398b6d8691982aa90b9f1376a38214030e52e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855215"
---
# <a name="c-style-strings"></a><span data-ttu-id="d38e1-103">Zeichen folgen im C-Stil</span><span class="sxs-lookup"><span data-stu-id="d38e1-103">C-Style Strings</span></span>

<span data-ttu-id="d38e1-104">Eine WinSNMP-Anwendung kann mit **null** endende Zeichen folgen im C-Stil zum Konvertieren von Entitäts-und objektbezeichnerobjekten (OID) in und aus ihren Zeichen folgen Darstellungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="d38e1-104">A WinSNMP application can use **NULL**-terminated C-style strings to convert entity and object identifier (OID) objects to and from their string representations.</span></span>

<span data-ttu-id="d38e1-105">Zu den WinSNMP-Funktionen, die Zeichen folgen im C-Stil bearbeiten, gehören [**snmpstreinentity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**snmpentitydestr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**snmpstrdeoid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)und [**snmpoiddestr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr).</span><span class="sxs-lookup"><span data-stu-id="d38e1-105">The WinSNMP functions that manipulate C-style strings include [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid), and [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr).</span></span> <span data-ttu-id="d38e1-106">Da [**snmpentitydestr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) und [**snmpoidesstr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) einen Zeiger auf eine Zeichen folgen Variable im C-Format zurückgeben, muss die WinSNMP-Anwendung einen entsprechenden Wert im *size* -Parameter übergeben, wenn diese Funktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d38e1-106">Because [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) and [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) return a pointer to a C-style string variable, the WinSNMP application must pass an appropriate value in the *size* parameter when it makes calls to these functions.</span></span> <span data-ttu-id="d38e1-107">Weitere Informationen finden Sie auf den Referenzseiten für diese Funktionen.</span><span class="sxs-lookup"><span data-stu-id="d38e1-107">For more information, see the reference pages for these functions.</span></span>

> [!Note]  
> <span data-ttu-id="d38e1-108">Der *Kontext* Parameter der [**snmpstrautcontext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) -Funktion und der [**snmpcontextdestr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) -Funktion muss eine Oktett-Zeichen folgen Struktur sein, d. h. eine [**smioctets**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d38e1-108">The *context* parameter of the [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) and [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) functions must be an octet string structure, that is, an [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) structure.</span></span> <span data-ttu-id="d38e1-109">Der *Kontext* Parameter darf keine Zeichenfolge im C-Format sein.</span><span class="sxs-lookup"><span data-stu-id="d38e1-109">The *context* parameter cannot be a C-style string.</span></span> <span data-ttu-id="d38e1-110">Die in einer **smioctets** -Struktur enthaltene Zeichenfolge erfordert kein Byte, das **null** endet.</span><span class="sxs-lookup"><span data-stu-id="d38e1-110">The string contained in an **smiOCTETS** structure does not require a **NULL**-terminating byte.</span></span>

 

 

 




