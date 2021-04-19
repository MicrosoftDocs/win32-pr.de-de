---
description: Wenn Sie benutzerdefinierte Erweiterungen erstellen oder eine komplexe Erweiterung codieren möchten, können Sie eigene Erweiterungs Handler schreiben, mit denen benutzerdefinierte Schnittstellen exportiert werden.
ms.assetid: a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b
title: Schreiben von benutzerdefinierten Erweiterungs Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c8c4380b11fd0b0b1a5484ba0a7ab80f69c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364160"
---
# <a name="writing-custom-extension-handlers"></a><span data-ttu-id="15806-103">Schreiben von benutzerdefinierten Erweiterungs Handlern</span><span class="sxs-lookup"><span data-stu-id="15806-103">Writing Custom Extension Handlers</span></span>

<span data-ttu-id="15806-104">Wenn Sie benutzerdefinierte Erweiterungen erstellen oder eine komplexe Erweiterung codieren möchten, können Sie eigene Erweiterungs Handler schreiben, mit denen benutzerdefinierte Schnittstellen exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="15806-104">To create custom extensions or to encode a complex extension, you can write your own extension handlers that export custom interfaces.</span></span> <span data-ttu-id="15806-105">Die Microsoft-Zertifikat Dienste werden mit den folgenden Schnittstellen ausgeliefert, die zum Codieren verschiedener Erweiterungs Datentypen verwendet werden können: [**icertencodealtname**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**icertencodebitstring**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**icertencodecrldistinfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**icertencodedatearray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**icertencodelta ongarray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)und [**icertencodestringarray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray).</span><span class="sxs-lookup"><span data-stu-id="15806-105">Microsoft Certificate Services ships with the following interfaces which can be used to encode various types of extension data: [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray), and [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray).</span></span> <span data-ttu-id="15806-106">Diese Schnittstellen sind in Certenc.dll enthalten.</span><span class="sxs-lookup"><span data-stu-id="15806-106">These interfaces are contained in Certenc.dll.</span></span> <span data-ttu-id="15806-107">Außerdem sind die Typinformationen für diese Schnittstellen in Certencl.dll enthalten, das im Platform Software Development Kit (SDK) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="15806-107">Additionally, the type information for these interfaces is contained in Certencl.dll, which is contained in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="15806-108">Weitere Informationen zu Erweiterungs Handlern finden Sie unter [Erweiterungs Handler](extension-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="15806-108">For more information about extension handlers, see [Extension Handlers](extension-handlers.md).</span></span>

 

 



