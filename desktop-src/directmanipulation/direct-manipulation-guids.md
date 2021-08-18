---
description: Die folgenden GUIDs der Direct Manipulation-Klasse sind in DirectManipulation.idl definiert.
ms.assetid: 6747D082-4B7B-4C7E-A230-2E8C8412FABD
title: GUIDs für die direkte Bearbeitung
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3ee67206bf9395c3a338dba27c9365578d30d7304f465d93fdc90322a77a8a0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280541"
---
# <a name="direct-manipulation-guids"></a>GUIDs für die direkte Bearbeitung

Die folgenden GUIDs der [Direct Manipulation-Klasse](direct-manipulation-portal.md) sind in DirectManipulation.idl definiert.

- [Masterklassen-IDs](#master-class-ids)
- [Klassen-IDs für sekundären Inhalt](#secondary-content-class-ids)
- [Verhaltensobjekte – Klassen-IDs](#behavior-objects-class-ids)
- [Zugehörige Themen](#related-topics)

## <a name="master-class-ids"></a>Masterklassen-IDs

| GUID                                     | Beschreibung                                                                                                                                                                                                                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **54E211B6-3650-4F75-8334-FA359598E1C5** | DirectManipulationManager-Klasse. Dieses Objekt bietet Zugriff auf alle Funktionen und APIs für [die direkte Bearbeitung,](direct-manipulation-portal.md) die der Anwendung zur Verfügung stehen.                                                                                                                         |
| **79DEA627-A08A-43AC-8EF5-6900B9299126** | DCompManipulationCompositor-Klasse. Dies ist eine Implementierung des [**IDirectManipulationCompositor,**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) der DirectComposition umschließt. Über dieses Compositorobjekt kann DirectManipulation die Ausgabe anwenden, indem Transformationen direkt auf die DComp-Struktur festgelegt werden. |

## <a name="secondary-content-class-ids"></a>Klassen-IDs für sekundären Inhalt

| GUID                                  | Beschreibung                                                                                                                      |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ VerticalIndicatorContent**   | Indikator für vertikales Schwenken. Ein visuelles Element, das Ihre aktuelle Position im Inhalt anzeigt, die sich vertikal außerhalb des Bildschirms erstreckt.     |
| **CLSID \_ HorizontalIndicatorContent** | Horizontaler Schwenkindikator. Ein visuelles Element, das Ihre aktuelle Position in Inhalten anzeigt, die sich horizontal außerhalb des Bildschirms erstreckt. |
| **CLSID \_ VirtualViewportContent**     | Virtueller Viewport. Ein virtueller Viewport kann verwendet werden, um Elemente mit fester Position für Viewports mit konfiguriertem Zoom zu berücksichtigen.          |

## <a name="behavior-objects-class-ids"></a>Verhaltensobjekte – Klassen-IDs

| GUID                                     | Beschreibung                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ DragDropConfigurationBehavior** | Ziehen Sie & Ablageverhalten. Ermöglicht das Auswählen und Ziehen von Elementen.                                                                                       |
| **CLSID \_ AutoScrollBehavior**            | Verhalten der automatischen Registrierung. Ermöglicht es Dem Inhalt, automatisch zu scrollen, wenn er sich der Grenze einer bestimmten Achse nähert.                                           |
| **CLSID \_ DeferContactService**           | Kontaktrückstellungsverhalten. Die Zeitspanne (in Milllisekunden), die gewartet werden soll, bevor [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)aufgerufen wird. |

## <a name="related-topics"></a>Zugehörige Themen

[Direkte Bearbeitung,](direct-manipulation-portal.md) [**ActivateConfiguration,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration) [**AddConfiguration,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration) [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor)
