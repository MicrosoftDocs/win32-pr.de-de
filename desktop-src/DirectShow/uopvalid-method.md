---
description: Die uopvalid-Methode ruft einen Wert ab, der angibt, ob der angegebene Benutzer Vorgang (User Operation, UOP) aktuell gültig ist.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: Uopvalid-Methode (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3051ad20c496713880407270c7054839520ce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359304"
---
# <a name="uopvalid-method"></a>Uopvalid-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `UOPValid` Methode ruft einen Wert ab, der angibt, ob der angegebene Benutzer Vorgang (User Operation, UOP) aktuell gültig ist.

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iuop*
</dt> <dd>

Gibt den Benutzer Vorgang (User Operation, UOP) als ganze Zahl an.



| Wert | BESCHREIBUNG                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | [**Playtitle**](playtitle-method.md), [**playattime**](playattime-method.md)[**playattimeingetitle**](playattimeintitle-method.md)                                                                                      |
| 1     | [**Playchapter**](playchapter-method.md)                                                                                                                                                                                |
| 2     | [**Playtitle**](playtitle-method.md)                                                                                                                                                                                    |
| 3     | [**Stop**](stop-method.md)                                                                                                                                                                                              |
| 4     | [**Returnfromsubmenu**](returnfromsubmenu-method.md)                                                                                                                                                                    |
| 5     | [**Playchapter**](playchapter-method.md)                                                                                                                                                                                |
| 6     | [**Playprevchapter**](playprevchapter-method.md), [ **replaychapter**](replaychapter-method.md)                                                                                                                         |
| 7     | [**Playnextchapter**](playnextchapter-method.md)                                                                                                                                                                        |
| 8     | [**Playforward**](playforwards-method.md)                                                                                                                                                                              |
| 9     | [**Playrückwärts**](playbackwards-method.md)                                                                                                                                                                            |
| 10    | [**Showmenu**](showmenu-method.md) mit dem Parameterwert 2 (DVD- \_ \_ Menütitel)                                                                                                                                       |
| 11    | [**Showmenu**](showmenu-method.md) mit einem Parameterwert von 3 (DVD- \_ Menü Stamm \_ )                                                                                                                                        |
| 12    | [**Showmenu**](showmenu-method.md) mit dem Parameterwert 4 (DVD- \_ Menü \_ Teilbild)                                                                                                                                  |
| 13    | [**Showmenu**](showmenu-method.md) mit dem Parameterwert 5 (DVD \_ -Menü \_ Audiodatei)                                                                                                                                       |
| 14    | [**Showmenu**](showmenu-method.md) mit dem Parameterwert 6 (DVD- \_ Menü \_ Winkel)                                                                                                                                       |
| 15    | [**Showmenu**](showmenu-method.md) mit einem Parameterwert von 7 (DVD- \_ Menü \_ Kapitel)                                                                                                                                     |
| 16    | [**Fortsetzen**](resume-method.md)                                                                                                                                                                                          |
| 17    | [**Selecbuchstabftbutton**](selectleftbutton-method.md), [**selecseleghtbutton**](selectrightbutton-method.md), [**selectupperbutton**](selectupperbutton-method.md), [**selectlowerbutton**](selectlowerbutton-method.md) |
| 18    | [**Stilloff**](stilloff-method.md)                                                                                                                                                                                      |
| 19    | [**Anhalten**](pause-method.md)                                                                                                                                                                                            |
| 20    | [**Currentaudiostream**](currentaudiostream-property.md)                                                                                                                                                                |
| 21    | [**Currentsubpicturestream**](currentsubpicturestream-property.md)                                                                                                                                                      |
| 22    | [**Currentangle**](currentangle-property.md), [ **selectparamevel**](selectparentallevel-method.md)                                                                                                                 |
| 23    | [**Karaokeaudiopressentiments ationmode**](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| 24    | Wählen Sie den Videomodus aus.                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob der angegebene Vorgang von einem UOP-Steuerelement zugelassen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Segment. h</dt> </dl> |



 

 




