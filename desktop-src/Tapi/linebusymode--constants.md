---
description: Die LINEBUSYMODE-Bitflags-Konstanten beschreiben verschiedene ausgelastete Signale, die der Switch \_ oder das Netzwerk generieren kann. Diese Ausgelastet-Signale weisen in der Regel darauf hin, dass derzeit eine andere Ressource verwendet wird, die für einen Aufruf erforderlich ist.
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: LINEBUSYMODE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54563567944a2e5164717f7d64ff7026a0045ea735405a7bcad159969f07514a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681990"
---
# <a name="linebusymode_-constants"></a>LINEBUSYMODE-Konstanten \_

Die **\_ LINEBUSYMODE-Bitflags-Konstanten** beschreiben verschiedene ausgelastete Signale, die der Switch oder das Netzwerk generieren kann. Diese Ausgelastet-Signale weisen in der Regel darauf hin, dass derzeit eine andere Ressource verwendet wird, die für einen Aufruf erforderlich ist.

<dl> <dt>

<span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**LINEBUSYMODE-STATION \_**
</dt> <dd> <dl> <dt>



Das Signal "Ausgelastet" gibt an, dass die Station der aufgerufenen Partei ausgelastet ist. Dies wird in der Regel mit einem normalen *ausgelasteten* Ton signalisiert.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**LINEBUSYMODE \_ TRUNK**
</dt> <dd> <dl> <dt>



Das Ausgelastet-Signal gibt an, dass ein Trunk oder eine Leitung ausgelastet ist. Dies wird in der Regel mit einem schnellen *ausgelasteten* Ton signalisiert.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE \_ UNKNOWN**
</dt> <dd> <dl> <dt>



Der spezifische Modus des ausgelastet-Signals ist derzeit unbekannt, wird aber möglicherweise später bekannt.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE \_ UNAVAIL**
</dt> <dd> <dl> <dt>



Der spezifische Modus des Ausgelastetsignals ist nicht verfügbar und wird nicht bekannt.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die hochwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden. Die niedrigen 16 Bits sind reserviert.

> [!Note]  
> Ausgelastete Signale können als Inband- oder Out-of-Band-Nachrichten gesendet werden. TAPI geht nicht vom spezifischen Signalisierungsmechanismus aus.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




