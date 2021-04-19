---
title: Interaktions Kontextfunktionen
description: Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für Interaktions Kontextfunktionen.
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
ms.openlocfilehash: 7f57bf6ac2b5d9bc7f17a43cd84a6e8eb7d828a4
ms.sourcegitcommit: 6b8d5058d02daacad4d2ed7830da63b63a509586
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/07/2020
ms.locfileid: "106342106"
---
# <a name="interaction-context-functions"></a>Interaktions Kontextfunktionen

Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für [Interaktions Kontext](interaction-context-portal.md) Funktionen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|---|---|
| [**Addpointerinteraktioncontext**](/windows/win32/api/interactioncontext/nf-interactioncontext-addpointerinteractioncontext)<br/> | Schließt den angegebenen Zeiger in den Satz von Zeigern ein, die vom [Interaktions Kontext](interaction-context-portal.md) Objekt verarbeitet werden. <br/> |
| [**Bufferpointerpacketsinteraction Context**](/windows/win32/api/interactioncontext/nf-interactioncontext-bufferpointerpacketsinteractioncontext)<br/> | Fügt dem Puffer des [Interaktions Kontext](interaction-context-portal.md) Objekts den Verlauf für einen einzelnen Eingabe Zeiger hinzu.<br/> |
| [**"Erstellungs Kontext"**](/windows/win32/api/interactioncontext/nf-interactioncontext-createinteractioncontext)<br/> | Erstellt und initialisiert ein [Interaktions Kontext](interaction-context-portal.md) Objekt.<br/> |
| [**Destroyinteraktioncontext**](/windows/win32/api/interactioncontext/nf-interactioncontext-destroyinteractioncontext)<br/> | Zerstört das angegebene [Interaktions Kontext](interaction-context-portal.md) Objekt.<br/> |
| [**Getcrossdiasparameterinteraction Context**](/windows/win32/api/interactioncontext/nf-interactioncontext-getcrossslideparameterinteractioncontext)<br/> | Ruft das Verhalten der Kreuz Folie Interaktion ab. <br/> |
| [**Getinertiaparameterinteraction Context**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinertiaparameterinteractioncontext)<br/> | Ruft das Trägheits Verhalten einer Manipulation (Übersetzung, Drehung, Skalierung) ab. <br/> |
| [**Getinteraktionconfigurationinteraktioncontext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinteractionconfigurationinteractioncontext)<br/> | Ruft den Interaktions Konfigurations Zustand für das [Interaktions Kontext](interaction-context-portal.md) Objekt ab.<br/> |
| [**Getmouswheelparameterinteraction Context**](/windows/win32/api/interactioncontext/nf-interactioncontext-getmousewheelparameterinteractioncontext)<br/> | Ruft den Mausrad Zustand für das [Interaktions Kontext](interaction-context-portal.md) Objekt ab. <br/> |
| [**Getpropertyinteraktioncontext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getpropertyinteractioncontext)<br/> | Ruft Eigenschaften des [Interaktions Kontext](interaction-context-portal.md) Objekts ab.<br/> |
| [**Getstatueingeteraction Context**](/windows/win32/api/interactioncontext/nf-interactioncontext-getstateinteractioncontext)<br/> | Ruft den aktuellen [Interaktions Kontext](interaction-context-portal.md) Zustand und die Uhrzeit ab, zu der der Kontext in den Leerlaufzustand wechselt. <br/> |
| [**Processbufferedpacketsinteraction Context**](/windows/win32/api/interactioncontext/nf-interactioncontext-processbufferedpacketsinteractioncontext)<br/> | Verarbeitet gepufferte Pakete am Ende eines Zeiger Eingabe Frames.<br/> |
| [**Processinertiainteraktioncontext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processinertiainteractioncontext)<br/> | Sendet Zeit Geber Eingaben an das [Interaktions Kontext](interaction-context-portal.md) Objekt für die Trägheits Verarbeitung.<br/> |
| [**Processpointerframesinteraktioncontext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processpointerframesinteractioncontext)<br/> | Verarbeitet eine Reihe von Zeiger Eingabe Frames.<br/> |
| [**Registeroutputcallbackinteraction Context**](/windows/win32/api/interactioncontext/nf-interactioncontext-registeroutputcallbackinteractioncontext)<br/> | Registriert einen Rückruf, um Interaktions Ereignisse von einem [Interaktions Kontext](interaction-context-portal.md) Objekt zu empfangen.<br/> |
| [**Removepointerinteraktioncontext**](/windows/win32/api/interactioncontext/nf-interactioncontext-removepointerinteractioncontext)<br/> | Entfernt den angegebenen Zeiger aus dem Satz von Zeigern, die vom [Interaktions Kontext](interaction-context-portal.md) Objekt verarbeitet werden. <br/> |
| [**Resetinteraktioncontext**](/windows/win32/api/interactioncontext/nf-interactioncontext-resetinteractioncontext)<br/> | Setzt den [**Interaktions Zustand**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state), die Interaktions Konfigurationseinstellungen und alle Parameter auf ihren ursprünglichen Zustand zurück. Aktuelle Interaktionen werden ohne Benachrichtigungen abgebrochen. <br/> Der [Interaktions Kontext](interaction-context-portal.md) muss vor der nächsten Verwendung neu konfiguriert werden.<br/> |
| [**Setcrossdiasparametersinteraction Context**](/windows/win32/api/interactioncontext/nf-interactioncontext-setcrossslideparametersinteractioncontext)<br/> | Konfiguriert die Kreuz Folie-Interaktion. <br/> |
| [**"" "".**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinertiaparameterinteractioncontext)<br/> | Konfiguriert das Trägheits Verhalten einer Manipulation (Übersetzung, Drehung, Skalierung), nachdem der Kontakt aufgehoben wurde. <br/> | [**Setinteraktionconfigurationinteraktioncontext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinteractionconfigurationinteractioncontext)<br/> | Konfiguriert das [Interaktions Kontext](interaction-context-portal.md) Objekt so, dass die angegebenen Manipulationen verarbeitet werden.<br/> |
| [**"Stmouswheelparameterinteraction Context"**](/windows/win32/api/interactioncontext/nf-interactioncontext-setmousewheelparameterinteractioncontext)<br/> | Legt die Parameterwerte für das Mausrad fest. <br/> |
| [**Setpivotinteraktioncontext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpivotinteractioncontext)<br/> | Legt den Mittelpunkt und den pivotradius vom Mittelpunkt für eine Rotations Bearbeitung mithilfe eines einzelnen Eingabe Zeigers fest. <br/> |
| [**Setpropertyinteraktioncontext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpropertyinteractioncontext)<br/> | Legt [Interaktions Kontext](interaction-context-portal.md) -Objekteigenschaften fest.<br/> |
| [**Stopinteraktioncontext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)<br/> | Legt den [**Interaktions Zustand**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state) auf den Interaktions \_ Zustand im \_ Leerlauf fest und lässt alle Interaktions Konfigurationseinstellungen und Parameter unverändert. Aktuelle Interaktionen werden abgebrochen und Benachrichtigungen gesendet, wenn dies erforderlich ist.<br/> Der [Interaktions Kontext](interaction-context-portal.md) muss vor der nächsten Verwendung nicht neu konfiguriert werden.<br/> |

## <a name="related-topics"></a>Zugehörige Themen

[Interaktions Kontext Verweis](interaction-context-reference.md)
