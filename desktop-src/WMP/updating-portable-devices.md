---
title: Aktualisieren von tragbaren Geräten
description: Aktualisieren von tragbaren Geräten
ms.assetid: 2827e71b-f5e9-4403-9763-043239c4a216
keywords:
- Windows Media Player Online Stores, Aktualisieren von tragbaren Geräten
- Online Stores, Aktualisieren von tragbaren Geräten
- Geben Sie 1 Online Stores ein, aktualisieren Sie tragbare Geräte.
- Windows Media Player Online Stores, portable Geräte
- Online Stores, portable Geräte
- Typ 1 Online Stores, portable Geräte
- Aktualisieren von tragbaren Geräten
- Portable Geräte, aktualisieren
- Portable Geräte, Windows Media Player Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b29f5314f4eba1af43b3858304f02f8a7e0107df
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314225"
---
# <a name="updating-portable-devices"></a>Aktualisieren von tragbaren Geräten

Windows Media Player ermöglicht Benutzern das Synchronisieren digitaler Medieninhalte mit tragbaren Geräten. Dies kann Musikinhalte enthalten, die in einem Online Store erworben oder gemietet wurden. Unter bestimmten Umständen möchten Online Store-Anbieter vielleicht Code schreiben, um auf einem verbundenen tragbaren Gerät als Teil der Verwaltung von Inhalten des Stores zu arbeiten. Um dem Online Shop-Plug-in die Gelegenheit zu geben, mit einem verbundenen Gerät zu arbeiten, ruft Windows Media Player [iwmpcontentpartner:: updatedevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) auf und gibt den kanonischen Namen des portablen Geräts an. Wenn der Plug-in-Code feststellt, dass die Arbeit mit dem verbundenen Gerät erledigt werden muss, muss er \_ vom **Update Device-Update** sofort den Wert OK zurückgeben, bevor die Arbeit fortgesetzt werden kann. Wenn keine Arbeit durchzuführen ist, sollte das Plug-in einen Fehlercode zurückgeben.

Wenn das Plug-in die Verwendung des Geräts abgeschlossen hat, muss es [iwmpcontentpartnercallback:: updatedevicecomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) aufrufen, um Windows Media Player zu benachrichtigen, dass das Gerät verfügbar ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmier Handbuch für den Typ 1 Online Stores**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




