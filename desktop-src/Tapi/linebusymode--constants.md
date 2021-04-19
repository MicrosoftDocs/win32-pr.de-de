---
description: Die linebusymode \_ -Bitflag-Konstanten beschreiben verschiedene ausgelastete Signale, die der Switch oder das Netzwerk generieren kann. Diese ausgelasteten Signale geben in der Regel an, dass eine andere Ressource, die für einen-Rückruf erforderlich ist, zurzeit verwendet wird.
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: LINEBUSYMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c996ad4e6142cc8312983945ae4c716ee0b35ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372482"
---
# <a name="linebusymode_-constants"></a>Linebusymode- \_ Konstanten

Die **linebusymode \_** -Bitflag-Konstanten beschreiben verschiedene ausgelastete Signale, die der Switch oder das Netzwerk generieren kann. Diese ausgelasteten Signale geben in der Regel an, dass eine andere Ressource, die für einen-Rückruf erforderlich ist, zurzeit verwendet wird.

<dl> <dt>

<span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**linebusymode- \_ Station**
</dt> <dd> <dl> <dt>



Das ausgelastete Signal gibt an, dass die Station der aufgerufenen Partei ausgelastet ist. Dies wird in der Regel mit einem *normalen* ausgelasteten Ton signalisiert.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**linebusymode- \_ trunk**
</dt> <dd> <dl> <dt>



Das ausgelastete Signal gibt an, dass ein trunk oder eine Verbindung ausgelastet ist. Dies wird in der Regel mit einem *fast* ausgelasteten Ton signalisiert.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**linebusymode \_ unbekannt**
</dt> <dd> <dl> <dt>



Der bestimmte Modus des ausgelasteten Signals ist zurzeit unbekannt, kann aber später bekannt werden.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**der Offline Modus ist \_ nicht erreichbar.**
</dt> <dd> <dl> <dt>



Der bestimmte Modus des ausgelasteten Signals ist nicht verfügbar und wird nicht bekannt werden.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden. Die nieder wertigen 16 Bits sind reserviert.

> [!Note]  
> Ausgelastete Signale können als Inband-Töne oder out-of-Band-Nachrichten gesendet werden. TAPI nimmt keine Annahmen über den spezifischen Signalisierungs Mechanismus vor.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




