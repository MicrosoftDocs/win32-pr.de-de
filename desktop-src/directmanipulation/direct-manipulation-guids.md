---
description: Die folgenden GUIDs der direkten Manipulations Klasse sind in "directmanipulation. idl" definiert.
ms.assetid: 6747D082-4B7B-4C7E-A230-2E8C8412FABD
title: GUIDs für direkte Manipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 57dfa5701d7f01a9738206e7a2e3d669f6cf6a4a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342551"
---
# <a name="direct-manipulation-guids"></a>GUIDs für direkte Manipulation

Die folgenden GUIDs der [direkten Manipulations](direct-manipulation-portal.md) Klasse sind in "directmanipulation. idl" definiert.

- [Master Klasse-IDs](#master-class-ids)
- [Sekundäre Inhalts Klasse-IDs](#secondary-content-class-ids)
- [Behavior-Objektklasse-IDs](#behavior-objects-class-ids)
- [Zugehörige Themen](#related-topics)

## <a name="master-class-ids"></a>Master Klasse-IDs

| GUID                                     | Beschreibung                                                                                                                                                                                                                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **54e211b6-3650-4t75-8334-fa359598e1c5** | Directmanipulationmanager-Klasse. Dieses Objekt ermöglicht den Zugriff auf alle [direkten Manipulations](direct-manipulation-portal.md) Features und APIs, die für die Anwendung verfügbar sind.                                                                                                                         |
| **79dea627-a08a-43ac-8ef5-6900b9299126** | Dcompmanipulationcompositor-Klasse. Dies ist eine Implementierung von [**idirectmanipulationcompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) , die directcomposition umschließt. Über dieses Compositor-Objekt kann directmanipulation die Ausgabe anwenden, indem Transformationen direkt in der Dcomp-Struktur festgelegt werden. |

## <a name="secondary-content-class-ids"></a>Sekundäre Inhalts Klasse-IDs

| GUID                                  | Beschreibung                                                                                                                      |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ verticalindikatorcontent**   | Vertikaler Schwenk Indikator. Ein visuelles Element, das die aktuelle Position im Inhalt anzeigt, der vertikal aus dem Bildschirm erweitert wird.     |
| **CLSID \_ horizontalindikatorcontent** | Horizontaler Schwenk Indikator. Ein visuelles Element, das die aktuelle Position im Inhalt anzeigt, der horizontal aus dem Bildschirm erweitert wird. |
| **CLSID \_ virtualviewportcontent**     | Virtueller Viewport. Ein virtueller Viewport kann verwendet werden, um fixierte Positions Elemente für Viewports mit konfiguriertem Zoomfaktor zu berücksichtigen.          |

## <a name="behavior-objects-class-ids"></a>Behavior-Objektklasse-IDs

| GUID                                     | Beschreibung                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ dragdropconfigurationbehavior** | Ziehen Sie & Drop-Verhalten. Ermöglicht das auswählen und ziehen von Elementen.                                                                                       |
| **CLSID- \_ autoscrollbehavior**            | AutoScroll-Verhalten. Ermöglicht, dass der Inhalt automatisch durch Scrollen wird, während er die Begrenzung einer bestimmten Achse nähert.                                           |
| **CLSID- \_ defercontactservice**           | Wenden Sie sich an das Verzögerungs Verhalten Die Zeitspanne (in milllisekunden), die gewartet werden soll, bevor [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)aufgerufen wird. |

## <a name="related-topics"></a>Zugehörige Themen

[Direkte Bearbeitung](direct-manipulation-portal.md), [**activateconfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration), [**addconfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration), [**idirectmanipulationcompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor)
