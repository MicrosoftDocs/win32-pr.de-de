---
title: NPS-Erweiterungsfunktionen
description: NPS-Erweiterungsfunktionen
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cecf8ead61e94287ba4846b82f922af40068a771a9bcadd8ccb51693709c17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362360"
---
# <a name="nps-extensions-functions"></a>NPS-Erweiterungsfunktionen

> [!Note]  
> Internet Authentication Service (IAS) wurde ab Windows Server 2008 in Network Policy Server (NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Diensts zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

## <a name="application-defined"></a>Anwendungsdefiniert

Die Architektur für NPS-Erweiterungs-DLLs unterstützt die folgenden exportierten Funktionen:

-   [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

Die [**Funktionen RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) und [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) sind optional.

Die Erweiterungs-DLL exportiert [**möglicherweise RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) anstelle von [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) oder [**RadiusExtensionProcessEx.**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)

Wenn die Erweiterungs-DLL [**RadiusExtensionProcessEx exportiert,**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)muss sie auch [**RadiusExtensionFreeAttributes exportieren.**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)

## <a name="system-defined"></a>Systemdefiniert

Wenn NPS eine Implementierung von [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)aufruft, übergibt NPS der Funktion einen Zeiger auf eine [**RADIUS EXTENSION CONTROL \_ \_ \_ BLOCK-Struktur.**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block)

Die [**RADIUS EXTENSION CONTROL \_ \_ \_ BLOCK-Struktur**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) enthält Funktionsze zeiger auf die folgenden Funktionen, die von NPS bereitgestellt werden:

-   [**GetRequest**](/previous-versions/ms688263(v=vs.85))
-   [**Getresponse**](/previous-versions/ms688270(v=vs.85))
-   [**SetResponseType**](/previous-versions/ms688462(v=vs.85))

Die Funktionen [**GetRequest und**](/previous-versions/ms688263(v=vs.85)) [**GetResponse geben**](/previous-versions/ms688270(v=vs.85)) Zeiger auf eine Struktur vom Typ [**RADIUS ATTRIBUTE ARRAY \_ \_ zurück.**](/windows/desktop/api/authif/ns-authif-radius_attribute_array)

Die [**RADIUS \_ ATTRIBUTE \_ ARRAY-Struktur**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) enthält Funktionsze zeiger auf die folgenden Funktionen, die von NPS bereitgestellt werden:

-   [**Add**](/previous-versions/ms688246(v=vs.85))
-   [**AttributeAt**](/previous-versions/ms688253(v=vs.85))
-   [**GetSize**](/previous-versions/ms688277(v=vs.85))
-   [**Insertat**](/previous-versions/ms688296(v=vs.85))
-   [**RemoveAt**](/previous-versions/ms688452(v=vs.85))
-   [**Setat**](/previous-versions/ms688456(v=vs.85))

 

 