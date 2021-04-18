---
title: XML-Sprachunterstützung
description: In diesem Abschnitt wird die Ebene der XML-Sprachunterstützung in WWS beschrieben.
ms.assetid: c3408c2a-6506-4a2e-8083-b4a0154a6918
keywords:
- XML-Sprachunterstützung für Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13425d2ed9c878c3a63dd5b5908ffbab4f2f177
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "106340546"
---
# <a name="xml-language-support"></a><span data-ttu-id="d9f5e-106">XML-Sprachunterstützung</span><span class="sxs-lookup"><span data-stu-id="d9f5e-106">XML Language Support</span></span>

<span data-ttu-id="d9f5e-107">In diesem Abschnitt wird die Ebene der XML-Sprachunterstützung in WWS beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d9f5e-107">This section describe level of XML Language support in WWS.</span></span>


<span data-ttu-id="d9f5e-108">Weitere Informationen finden Sie in den Funktionen downlevellcidtolocalename in früheren Windows-Versionen als Windows Vista und lcidtolocalname, um zwischen einem LCID-Wert und einem XML: lang-Wert zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="d9f5e-108">See the functions DownlevelLCIDToLocaleName on versions of Windows earlier than Windows Vista, and LCIDToLocalName otherwise, to convert between an LCID and an xml:lang value.</span></span>

<span data-ttu-id="d9f5e-109">Beim lesen kann [**wsgetxmlattribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) verwendet werden, um den Wert eines "XML: lang"-Attributs im Bereich zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="d9f5e-109">When reading, [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) may be used to discover the value of an "xml:lang" attribute in scope.</span></span>

<span data-ttu-id="d9f5e-110">Beim Schreiben von kann [**wswritestartattribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) zum Schreiben eines "XML: lang"-Attributs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9f5e-110">When writing, [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) may be used to write an "xml:lang" attribute.</span></span>

 

 




