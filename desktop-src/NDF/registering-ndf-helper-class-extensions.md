---
title: Registrieren von NDF-Hilfsklassen Erweiterungen
description: Jeder Hilfsklassen Erweiterung sind mehrere Registrierungsschlüssel zugeordnet. Einige Schlüssel sind für com erforderlich, und einige Schlüssel sind für die NDF erforderlich.
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f211517a975bdef61db7937fffa95f13beddc156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714670"
---
# <a name="registering-ndf-helper-class-extensions"></a>Registrieren von NDF-Hilfsklassen Erweiterungen

Jeder Hilfsklassen Erweiterung sind mehrere Registrierungsschlüssel zugeordnet. Einige Schlüssel sind für com erforderlich, und einige Schlüssel sind für die NDF erforderlich.

## <a name="com-registry-keys"></a>COM-Registrierungsschlüssel

Hilfsklassen Erweiterungen müssen als com-Server implementiert werden. Die com-Registrierung muss für jede hilfsklassenerweiterung abgeschlossen werden. Die CLSID des Objekts, die [**inetdiaghelperinfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) -Schnittstelle und die [**inetdiaghelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) -Schnittstelle müssen registriert werden. Bei der Registrierung wird eine Reihe von com-bezogenen Registrierungs Schlüsseln für die NDF-hilfsklassenerweiterung erstellt.

## <a name="ndf-registry-keys"></a>NDF-Registrierungsschlüssel

Hilfsklassen Erweiterungen müssen registriert werden, bevor Sie mit dem Netzwerk Diagnose Framework und mit anderen verwandten Hilfsklassen interagieren können. Dies wird durch Auffüllen der Registrierung erreicht.

Im folgenden Verfahren wird gezeigt, wie Sie der Registrierung Hilfsklassen Erweiterungen hinzufügen.

1.  Veröffentlichen Sie die Namen der von der dll implementierten Hilfsklassen und ihrer Abhängigkeiten, indem Sie einen Schlüssel für die dll unter erstellen.

    **HKLM \\ System \\ CurrentControlSet- \\ Steuerelement \\ netdiagfx** \\ *VendorName* \\ **hostdlls** \\ *Hilfsklasse dll* \\ **helperclasses** \\ *Hilfsklassenname*

    Ersetzen Sie *VendorName*, *Helper Class dll* und *Helper Class Name* durch benutzerdefinierte Werte, wie unten beschrieben.

    | Wert               | type    | Bedeutung                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | *VendorName*        | REG- \_ SZ | Der Name des Herstellers.                                                      |
    | *Hilfsklassen-dll*  | REG- \_ SZ | Der Name der DLL ohne Erweiterung.                                          |
    | *Name der Hilfsklasse* | REG- \_ SZ | Der Name der Hilfsklasse, von der die aktuelle Hilfsklasse abhängt. |

    

     

2.  Veröffentlichen Sie unter jedem Namen Schlüssel der *Hilfsprogrammklasse* die folgenden Informationen.

    

    | Wert         | type       | Bedeutung                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **CLSID**     | REG- \_ SZ    | Eine Zeichenfolge, die die com-Klassen-ID der Hilfsklasse enthält.                                                                                                            |
    | **Version**   | REG- \_ SZ    | Eine Zeichenfolge, die die Haupt-und neben Versionen der Hilfsklasse im-Format enthält <major> <minor> .                                                        |
    | **Enes** | REG \_ DWORD | Der Wert 1 bedeutet, dass diese Hilfsklasse direkt vom Diagnose Client aufgerufen werden soll. der Wert 0 bedeutet, dass er nur von einer anderen Hilfsklasse aufgerufen werden kann. |
    | **Parent**    | REG- \_ SZ    | Eine Zeichenfolge, die die Microsoft Extensible Helper-Klasse benennt, die erweitert wird.                                                                                       |

    

     

3.  Veröffentlichen Sie für jede Hilfsklasse die Liste der übereinstimmenden Attribute, indem Sie einen Schlüssel unter

    **HKLM \\ System \\ CurrentControlSet \\ Control \\ netdiagfx** \\ *VendorName* \\ **hostdlls** \\ *Hilfsklasse dll* \\ **helperclasses** \\ *Hilfsklassen Name* \\ **MatchAttribute**

    Der Schlüssel muss mindestens einen Wert (einen pro Attribut) des folgenden Typs enthalten.

    | Wert             | type                             | Bedeutung                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | **AttributeName** | reg \_ SZ \| reg \_ DWORD \| reg \_ Binär | Ein-Wert, der das Name-Wert-Paar für ein bestimmtes Attribut abschließt. |

    

     

 

 




