---
description: Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für Zeiger Geräte-Eingabe Stapel Funktionen.
ms.assetid: 44942954-3EA6-4C33-8CF1-E8BF72A914CB
title: Funktionen (Eingabe Stapel für Zeiger Geräte)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: cfba2a0011747402af81d1f1379076282b65ca74
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106367163"
---
# <a name="pointer-device-input-stack-functions"></a>Eingabe Stapel Funktionen für Zeiger Geräte

Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für [Zeiger Geräte-Eingabe Stapel](pointer-device-stack-portal.md) Funktionen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|---|---|
| [**"Kreatesynderticpointerdevice"**](/windows/win32/api/winuser/nf-winuser-createsyntheticpointerdevice)<br/> | Konfiguriert das Zeiger einschleusungs Gerät für die aufrufenden Anwendung und initialisiert die maximale Anzahl gleichzeitiger Zeiger, die von der app eingefügt werden können.<br/> |
| [**Destroysyntheticpointerdevice**](/windows/win32/api/winuser/nf-winuser-destroysyntheticpointerdevice)<br/> | Zerstört das angegebene Zeiger einschleusungs Gerät.<br/> |
| [**Getpointerdevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice)<br/> | Ruft Informationen zum Zeiger Gerät ab.<br/> |
| [**Getpointerde vicecursoren**](/windows/win32/api/winuser/nf-winuser-getpointerdevicecursors)<br/> | Ruft die Cursor-IDs ab, die den einem Zeiger Gerät zugeordneten Cursorn zugeordnet sind.<br/> |
| [**Getpointerdeviceproperties**](/windows/win32/api/winuser/nf-winuser-getpointerdeviceproperties)<br/> | Ruft Geräteeigenschaften ab, die nicht in der [**Zeiger \_ Geräte \_ Informations**](/previous-versions/windows/desktop/api) Struktur enthalten sind. <br/> |
| [**Getpointerdevicerects**](/windows/win32/api/winuser/nf-winuser-getpointerdevicerects)<br/> | Ruft den x-und y-Bereich für das Zeiger Gerät (in HIMETRIC) und den x-und y-Bereich (aktuelle Auflösung) für die Anzeige ab, der das Zeiger Gerät zugeordnet ist. <br/> |
| [**Getpointerdevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices)<br/> | Ruft Informationen zu den Zeiger Geräten ab, die an das System angefügt sind.<br/> |
| [**Getrawpointerdevicedata**](/windows/win32/api/winuser/nf-winuser-getrawpointerdevicedata)<br/> | Ruft die unformatierten Eingabedaten vom Zeiger Gerät ab. <br/> |
| [**Injetsyntheticpointerinput**](/windows/win32/api/winuser/nf-winuser-injectsyntheticpointerinput)<br/> | Simuliert Zeiger Eingaben (Stift oder berühren).<br/> |
| [**Registerpointerdevicenotifications**](/windows/win32/api/winuser/nf-winuser-registerpointerdevicenotifications)<br/> | Registriert ein Fenster, in dem die Geräte Benachrichtigungen [**WM_POINTERDEVICECHANGE**](../inputmsg/wm-pointerdevicechange.md), [**WM_POINTERDEVICEINRANGE**](../inputmsg/wm-pointerdeviceinrange.md)und [**WM_POINTERDEVICEOUTOFRANGE**](../inputmsg/wm-pointerdeviceoutofrange.md) Zeiger verarbeitet werden.<br/> |

## <a name="related-topics"></a>Zugehörige Themen

[Verweis auf Zeiger Geräte-Eingabe Stapel Referenz](unified-input-stack-reference.md)
