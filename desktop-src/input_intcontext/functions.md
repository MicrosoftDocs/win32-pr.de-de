---
title: Interaktionskontextfunktionen
description: Die Themen in diesem Abschnitt enthalten die Referenzspezifikationen für Interaktionskontextfunktionen.
ms.assetid: 0F34F181-D92C-4B08-9F1D-62379D4A2B15
keywords:
- Benutzereingriff
- input
- Zeiger
- Toucheingabe
- Maus
- Stift
- Tablettstift
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: 5f0769aa5b9b097b23206c0515bd32552a59969404e72bbfcf26973d5d4f3de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758336"
---
# <a name="interaction-context-functions"></a>Interaktionskontextfunktionen

Die Themen in diesem Abschnitt enthalten die Referenzspezifikationen für [Interaktionskontextfunktionen.](interaction-context-portal.md)

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|---|---|
| [**AddPointerInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-addpointerinteractioncontext)<br/> | Schließen Sie den angegebenen Zeiger in den Satz von Zeigern ein, die vom [Interaktionskontextobjekt verarbeitet](interaction-context-portal.md) werden. <br/> |
| [**BufferPointerPacketsInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-bufferpointerpacketsinteractioncontext)<br/> | Fügt dem Puffer des Interaktionskontextobjekts den Verlauf für einen einzelnen [Eingabezeiger](interaction-context-portal.md) hinzu.<br/> |
| [**CreateInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-createinteractioncontext)<br/> | Erstellt und initialisiert ein [Interaktionskontextobjekt.](interaction-context-portal.md)<br/> |
| [**DestroyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-destroyinteractioncontext)<br/> | Zerstört das angegebene [Interaktionskontextobjekt.](interaction-context-portal.md)<br/> |
| [**GetCrossSlideParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getcrossslideparameterinteractioncontext)<br/> | Ruft das schiebeübergreifende Interaktionsverhalten ab. <br/> |
| [**GetInertiaParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinertiaparameterinteractioncontext)<br/> | Ruft das Trägheitsverhalten einer Manipulation ab (Übersetzung, Drehung, Skalierung). <br/> |
| [**GetInteractionConfigurationInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinteractionconfigurationinteractioncontext)<br/> | Ruft den Interaktionskonfigurationszustand für das [Interaktionskontextobjekt](interaction-context-portal.md) ab.<br/> |
| [**GetMouseWheelParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getmousewheelparameterinteractioncontext)<br/> | Ruft den Mausradzustand für das [Interaktionskontextobjekt](interaction-context-portal.md) ab. <br/> |
| [**GetPropertyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getpropertyinteractioncontext)<br/> | Ruft Eigenschaften [des Interaktionskontextobjekts](interaction-context-portal.md) ab.<br/> |
| [**GetStateInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getstateinteractioncontext)<br/> | Ruft den aktuellen [Interaktionskontextstatus](interaction-context-portal.md) und die Uhrzeit ab, zu der der Kontext in den Leerlaufzustand zurückwechselt. <br/> |
| [**ProcessBufferedPacketsInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processbufferedpacketsinteractioncontext)<br/> | Verarbeiten Sie gepufferte Pakete am Ende eines Zeigereingaberahmens.<br/> |
| [**ProcessInertiaInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processinertiainteractioncontext)<br/> | Sendet eine Timereingabe an das [Interaktionskontextobjekt](interaction-context-portal.md) für die Trägheitsverarbeitung.<br/> |
| [**ProcessPointerFramesInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processpointerframesinteractioncontext)<br/> | Verarbeitet einen Satz von Zeigereingabeframes.<br/> |
| [**RegisterOutputCallbackInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-registeroutputcallbackinteractioncontext)<br/> | Registriert einen Rückruf, um Interaktionsereignisse von einem [Interaktionskontextobjekt zu](interaction-context-portal.md) empfangen.<br/> |
| [**RemovePointerInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-removepointerinteractioncontext)<br/> | Entfernen Sie den angegebenen Zeiger aus dem Satz von Zeigern, die vom [Interaktionskontextobjekt verarbeitet](interaction-context-portal.md) werden. <br/> |
| [**ResetInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-resetinteractioncontext)<br/> | Setzt den [**Interaktionszustand,**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state)die Konfigurationseinstellungen für die Interaktion und alle Parameter auf ihren ursprünglichen Zustand zurück. Aktuelle Interaktionen werden ohne Benachrichtigungen abgebrochen. <br/> [Der Interaktionskontext](interaction-context-portal.md) muss vor der nächsten Verwendung neu konfiguriert werden.<br/> |
| [**SetCrossSlideParametersInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setcrossslideparametersinteractioncontext)<br/> | Konfiguriert die schiebeübergreifende Interaktion. <br/> |
| [**SetInertiaParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinertiaparameterinteractioncontext)<br/> | Konfiguriert das Trägheitsverhalten einer Manipulation (Übersetzung, Drehung, Skalierung), nachdem der Kontakt aufgehoben wurde. <br/> | [**SetInteractionConfigurationInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinteractionconfigurationinteractioncontext)<br/> | Konfiguriert das [Interaktionskontextobjekt](interaction-context-portal.md) für die Verarbeitung der angegebenen Bearbeitungen.<br/> |
| [**SetMouseWheelParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setmousewheelparameterinteractioncontext)<br/> | Legt die Parameterwerte für die Mausradeingabe fest. <br/> |
| [**SetPivotInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpivotinteractioncontext)<br/> | Legt den Mittelpunkt und den Pivotradius vom Mittelpunkt für eine Drehungsbearbeitung mit einem einzelnen Eingabezeiger fest. <br/> |
| [**SetPropertyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpropertyinteractioncontext)<br/> | Legt [Eigenschaften des Interaktionskontextobjekts](interaction-context-portal.md) fest.<br/> |
| [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)<br/> | Legt den [**Interaktionszustand auf**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state) INTERACTION \_ STATE IDLE fest und lässt alle \_ Konfigurationseinstellungen und Parameter der Interaktion intakt. Aktuelle Interaktionen werden abgebrochen, und Benachrichtigungen werden nach Bedarf gesendet.<br/> [Der Interaktionskontext](interaction-context-portal.md) muss vor der nächsten Verwendung nicht neu konfiguriert werden.<br/> |

## <a name="related-topics"></a>Zugehörige Themen

[Referenz zum Interaktionskontext](interaction-context-reference.md)
