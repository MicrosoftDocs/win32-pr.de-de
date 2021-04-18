---
title: NPS-Erweiterungsfunktionen
description: NPS-Erweiterungsfunktionen
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a20b424b8ef5109cea7f4d00b97f1a545b89ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338476"
---
# <a name="nps-extensions-functions"></a>NPS-Erweiterungsfunktionen

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

## <a name="application-defined"></a>Anwendung definiert

Die Architektur für NPS-Erweiterungs-DLLs unterstützt die folgenden exportierten Funktionen:

-   [**Radiusextensionfreattribute**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [**Radiusextensioninit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [**Radiusextensionprocess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [**Radiusextensionprocessex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [**Radiusextensionterm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

Die Funktionen [**radiusextensioninit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) und [**radiusextensionterm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) sind optional.

Die Erweiterungs-DLL kann [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) anstelle von [**radiusextensionprocess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) oder [**radiusextensionprocessex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)exportieren.

Wenn die Erweiterungs-DLL [**radiusextensionprocessex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)exportiert, muss auch [**radiusextensionfretribute**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)exportiert werden.

## <a name="system-defined"></a>System definiert

Wenn NPS eine Implementierung von [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)aufruft, übergibt NPS der Funktion einen Zeiger auf eine [**RADIUS- \_ Erweiterungs \_ Steuerungs \_ Block**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) Struktur.

Die [**RADIUS- \_ Erweiterungs \_ Steuerungs \_ Block**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) -Struktur enthält Funktionszeiger auf die folgenden Funktionen, die von NPS bereitgestellt werden:

-   [**GetRequest**](/previous-versions/ms688263(v=vs.85))
-   [**GetResponse**](/previous-versions/ms688270(v=vs.85))
-   [**Der Typ ""**](/previous-versions/ms688462(v=vs.85))

Die Funktionen [**GetRequest**](/previous-versions/ms688263(v=vs.85)) und [**GetResponse**](/previous-versions/ms688270(v=vs.85)) geben Zeiger auf eine Struktur vom Typ [**RADIUS- \_ Attribut \_ Array**](/windows/desktop/api/authif/ns-authif-radius_attribute_array)zurück.

Die [**Array Struktur des RADIUS- \_ Attributs \_**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) enthält Funktionszeiger auf die folgenden Funktionen, die von NPS bereitgestellt werden:

-   [**Hinzufügen**](/previous-versions/ms688246(v=vs.85))
-   [**Attributeat**](/previous-versions/ms688253(v=vs.85))
-   [**GetSize**](/previous-versions/ms688277(v=vs.85))
-   [**InsertAt**](/previous-versions/ms688296(v=vs.85))
-   [**RemoveAt**](/previous-versions/ms688452(v=vs.85))
-   [**SetAt**](/previous-versions/ms688456(v=vs.85))

 

 