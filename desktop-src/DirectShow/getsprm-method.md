---
description: Die GetSPRM-Methode ruft das angegebene Systemparameterregister ab.
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: GetSPRM-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e254d23f0d70890516bc5655f6c4ea38133a8a3733360955cabf9040207f3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536990"
---
# <a name="getsprm-method"></a>GetSPRM-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `GetSPRM` -Methode ruft das angegebene Systemparameterregister ab.

``` syntax
[ iSPRM = ] MSWebDVD.GetSPRM(iIndex)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Gibt das Register an, dessen Wert Sie als ganze Zahl abrufen möchten. Die ganze Zahl muss zwischen 0 und 23 liegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der den Inhalt des angegebenen Registers darstellt.

## <a name="remarks"></a>Hinweise

Der Datenträger steuert Systemparameterregister (SPRMs). Eine Playeranwendung muss für standardige Navigationsfunktionen nicht auf diese Register zugreifen. SPRMs stellen den Status des Players dar. Jede hat eine Bedeutung, die durch Benutzereinstellungen, Datenträgerbefehle und andere Vorkommen festgelegt wird, über die eine Anwendung keine direkte Kontrolle hat. Eine Anwendung kann diese Register lesen, aber nicht in sie schreiben. Um diese Register effektiv zu verwenden, benötigen Sie wahrscheinlich detailliertere Kenntnisse der DVD-Navigationsbefehle als in dieser Dokumentation angegeben. In der folgenden Tabelle sind die Inhalte der einzelnen Register aufgeführt. Ausführlichere Informationen zu den Registerinhalten finden Sie unter [ **IDvdInfo2::GetAllSPRMs.**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)



| Registrieren | Inhalte                        |
|----------|---------------------------------|
| 0        | Menüsprachcode              |
| 1        | Audiostreamnummer             |
| 2        | Subpicture-Datenstromnummer        |
| 3        | Aktuelle Winkelzahl            |
| 4        | Aktuelle Titelnummer            |
| 5        | Titelnummer                    |
| 6        | PGC-Nummer                      |
| 7        | Aktuelle Kapitelnummer (PTT)    |
| 8        | Hervorgehobene Schaltflächennummer       |
| 9        | Navigations-Timer                |
| 10       | PGC-Sprung für Navigation. Timer         |
| 11       | Audiopräsentationsmodus "Audio" |
| 12       | PML-Länder-/-Region-Code         |
| 13       | Pml                             |
| 14       | Videoeinstellung                   |
| 15       | Audiofunktion                |
| 16       | Audiosprache                  |
| 17       | Audiospracherweiterung        |
| 18       | Unterbildsprache             |
| 19       | Subpicture-Spracherweiterung   |
| 20       | Code der Playerregion              |
| 21       | Reserviert                        |
| 22       | Reserviert                        |
| 23       | Reserviert                        |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetGPRM**](getgprm-method.md)
</dt> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



