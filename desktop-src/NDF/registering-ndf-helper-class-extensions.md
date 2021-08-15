---
title: Registrieren von NDF-Hilfsklassenerweiterungen
description: Jeder Hilfsklassenerweiterung sind mehrere Registrierungsschlüssel zugeordnet. Einige Schlüssel sind für COM und einige Schlüssel für NDF erforderlich.
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6457e144abdeb1dbed1e33bb10e21302f918da8cdc5a6fd2090f3665e83f0316
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798497"
---
# <a name="registering-ndf-helper-class-extensions"></a>Registrieren von NDF-Hilfsklassenerweiterungen

Jeder Hilfsklassenerweiterung sind mehrere Registrierungsschlüssel zugeordnet. Einige Schlüssel sind für COM und einige Schlüssel für NDF erforderlich.

## <a name="com-registry-keys"></a>COM-Registrierungsschlüssel

Hilfsklassenerweiterungen müssen als COM-Server implementiert werden. Die COM-Registrierung muss für jede Hilfsklassenerweiterung abgeschlossen werden. Die CLSID des Objekts, die [**INetDiagHelperInfo-Schnittstelle**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) und die [**INetDiagHelper-Schnittstelle**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) müssen registriert werden. Die Registrierung erstellt eine Reihe von COM-bezogenen Registrierungsschlüsseln für die NDF-Hilfsklassenerweiterung.

## <a name="ndf-registry-keys"></a>NDF-Registrierungsschlüssel

Hilfsklassenerweiterungen müssen registriert werden, bevor sie mit dem Netzwerkdiagnoseframework und anderen verwandten Hilfsklassen interagieren. Dies wird erreicht, indem die Registrierung aufgefüllt wird.

Das folgende Verfahren zeigt, wie Sie der Registrierung Hilfsklassenerweiterungen hinzufügen.

1.  Veröffentlichen Sie die Namen der von der DLL implementierten Hilfsklassen und deren Abhängigkeiten, indem Sie unter einen Schlüssel für die DLL erstellen.

    **HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper Class DLL* \\ **HelperClasses** \\ *Helper Class Name*

    Ersetzen Sie *VendorName*, *Helper Class DLL* und *Helper Class Name* wie unten beschrieben durch benutzerdefinierte Werte.

    | Wert               | type    | Bedeutung                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | *VendorName*        | REG \_ SZ | Der Name des Herstellers.                                                      |
    | *Hilfsklassen-DLL*  | REG \_ SZ | Name der DLL ohne Erweiterung.                                          |
    | *Name der Hilfsklasse* | REG \_ SZ | Der Name der Hilfsklasse, von der die aktuelle Hilfsklasse abhängig ist. |

    

     

2.  Veröffentlichen Sie unter jedem *Helper Class Name-Schlüssel* die folgenden Informationen.

    

    | Wert         | type       | Bedeutung                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **Clsid**     | REG \_ SZ    | Eine Zeichenfolge, die die COM-Klassen-ID der Hilfsklasse enthält.                                                                                                            |
    | **Version**   | REG \_ SZ    | Eine Zeichenfolge, die die Haupt- und Nebenversionen der Hilfsklasse im Format <major> <minor> enthält.                                                        |
    | **Veröffentlicht** | REG \_ DWORD | Der Wert 1 bedeutet, dass erwartet wird, dass diese Hilfsklasse direkt vom Diagnoseclient aufgerufen wird. 0 bedeutet, dass es nur von einer anderen Hilfsklasse aufgerufen werden kann. |
    | **Parent**    | REG \_ SZ    | Eine Zeichenfolge, die die erweiterbare Hilfsklasse von Microsoft benennt, die erweitert wird.                                                                                       |

    

     

3.  Veröffentlichen Sie für jede Hilfsklasse die Liste der übereinstimmenden Attribute, indem Sie unter einen Schlüssel erstellen.

    **HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper Class DLL* \\ **HelperClasses** \\ *Helper Class Name* \\ **MatchAttributes**

    Sie müssen mindestens einen Wert (einen pro Attribut) des folgenden Typs enthalten.

    | Wert             | type                             | Bedeutung                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | **AttributeName** | REG \_ SZ \| REG \_ DWORD \| REG \_ BINARY | Ein -Wert, der das Name-Wert-Paar für ein bestimmtes Attribut vervollständigt. |

    

     

 

 




