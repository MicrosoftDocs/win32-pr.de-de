---
description: Die getsprm-Methode ruft das angegebene Systemparameter Register ab.
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: Getsprm-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8b6898902eda55e0e877878343a25d82d03660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957722"
---
# <a name="getsprm-method"></a>Getsprm-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `GetSPRM` Methode ruft das angegebene Systemparameter Register ab.

``` syntax
[ iSPRM = ] MSWebDVD.GetSPRM(iIndex)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Gibt das Register an, dessen Wert Sie als ganze Zahl abrufen möchten. Der ganzzahlige Wert muss zwischen 0 und 23 liegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der den Inhalt des angegebenen Registers darstellt.

## <a name="remarks"></a>Bemerkungen

Der Disc steuert die Systemparameter Register (sprms). Eine Player Anwendung muss nicht auf diese Register für eine standardmäßige Navigations Funktionalität zugreifen. Sprms stellt den Status des Players dar. Jede verfügt über eine Bedeutung, die durch Benutzereinstellungen, Disk-Befehle und andere vorkommen, auf die eine Anwendung keine direkte Kontrolle hat, festgelegt ist. Eine Anwendung kann diese Register lesen, aber nicht in Sie schreiben. Um diese Register effektiv zu verwenden, benötigen Sie wahrscheinlich ausführlichere Informationen über die DVD-Navigations Befehle als in dieser Dokumentation bereitgestellt werden. In der folgenden Tabelle werden die Inhalte der einzelnen Register aufgeführt. Ausführlichere Informationen zum Register Inhalt finden Sie unter [ **IDvdInfo2:: getallsprms**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)



| Registrieren | Inhalte                        |
|----------|---------------------------------|
| 0        | Menü Sprachcode              |
| 1        | Audiostreamnummer             |
| 2        | Subbild-streamnummer        |
| 3        | Aktuelle Winkel Zahl            |
| 4        | Aktuelle Titel Nummer            |
| 5        | Titel Nummer                    |
| 6        | PGC-Nummer                      |
| 7        | Aktuelle Kapitel Nummer (PTT)    |
| 8        | Markierte Schaltflächen Nummer       |
| 9        | Navigationszeit Geber                |
| 10       | PGC-Sprung für Navigations Tool. Timer         |
| 11       | Modus für die Karaoke-Audiopräsentation |
| 12       | PML-Land-/Regionscode         |
| 13       | PML                             |
| 14       | Video Einstellung                   |
| 15       | Audiofunktion                |
| 16       | Audiosprache                  |
| 17       | Erweiterung für Audiosprache        |
| 18       | Unter Bildsprache             |
| 19       | Teil Bild Spracherweiterung   |
| 20       | Player Regions Code              |
| 21       | Reserviert                        |
| 22       | Reserviert                        |
| 23       | Reserviert                        |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getgprm**](getgprm-method.md)
</dt> <dt>

[**Setgprm**](setgprm-method.md)
</dt> </dl>

 

 



