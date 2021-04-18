---
description: Die LINECALLFEATURE2 \_ -Konstanten Listen die ergänzenden Features auf, die für Konferenz-, Übertragungs-und Park Anrufe verfügbar sind.
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: LINECALLFEATURE2_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977e71f722fba34da6b2ecbd6a3e914c34a0aae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357671"
---
# <a name="linecallfeature2_-constants"></a>LINECALLFEATURE2- \_ Konstanten

Die **LINECALLFEATURE2 \_** -Konstanten Listen die ergänzenden Features auf, die für Konferenz-, Übertragungs-und Park Anrufe verfügbar sind.

<dl> <dt>

<span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2 \_ complcallback**
</dt> <dd> <dl> <dt>



Wenn dieses Bit aktiviert ist, kann das "Callback"-Feature mithilfe der linecomplmode- \_ Rückrufoption mit [**linecompletecallaufgerufen**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)werden. Das \_ completecallbit linecallfeature wird auch im **dwcallfeatures** -Member aktiviert.


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2 \_ complcampon**
</dt> <dd> <dl> <dt>



Wenn dieses Bit aktiviert ist, kann das Feature "Camp on" mithilfe der Option "-Option für linecomplmode" \_ mit [**linecompletecallaufgerufen**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)werden. Das \_ completecallbit linecallfeature wird auch im **dwcallfeatures** -Member aktiviert.


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2 \_ complintrude**
</dt> <dd> <dl> <dt>



Wenn dieses Bit aktiviert ist, kann das "Intrude"-Feature mithilfe der Option linecomplmode \_ Intrude mit [**linecompletecallaufgerufen**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)werden. Das \_ completecallbit linecallfeature wird auch im **dwcallfeatures** -Member aktiviert.


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2 \_ complmessage**
</dt> <dd> <dl> <dt>



Wenn dieses Bit aktiviert ist, kann die Funktion "Nachricht verlassen" mithilfe der Option "linecomplmode \_ Message" mit [**linecompletecallaufgerufen**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)werden. Das \_ completecallbit linecallfeature wird auch im **dwcallfeatures** -Member aktiviert.


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2 \_ noholdconference**
</dt> <dd> <dl> <dt>



Wenn dieses Bit aktiviert ist, kann eine "keine Hold-Konferenz" mithilfe der Option "linecallparamflags \_ noholdconference" mit [**linesetupconference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)erstellt werden. Das linecallfeature \_ setupconf-Bit wird auch im **dwcallfeatures** -Member aktiviert.


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2 \_ onesteptransfer**
</dt> <dd> <dl> <dt>



Wenn dieses Bit aktiviert ist, kann "One Step Transfer" mithilfe der linecallparamflags \_ onesteptransfer-Option mit [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)erstellt werden. Das linecallfeature \_ setuptransfer-Bit wird auch im **dwcallfeatures** -Member aktiviert.

> [!Note]  
> Wenn keines der compl-Bits im **dwCallFeatures2** -Member in [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) angegeben ist, aber linecallfeature \_ completecallfest gelegt ist, ist es möglich, dass jeder dieser Komponenten funktioniert, aber der Dienstanbieter hat nicht angegeben.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2 \_ transferconf**
</dt> <dd> <dl> <dt>



Wenn dieses Bit ist, kann die Funktion [**linecompletetransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) verwendet werden, um die Übertragung als drei-Wege-Konferenz aufzulösen. Das \_ completetransf-Bit linecallfeature wird auch im **dwcallfeatures** -Member aktiviert.


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2 \_ transfernorm**
</dt> <dd> <dl> <dt>



Wenn dieses Bit ist, kann die Funktion [**linecompletetransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) verwendet werden, um die Übertragung als normale Übertragung zu beheben. Das \_ completetransf-Bit linecallfeature wird auch im **dwcallfeatures** -Member aktiviert.

> [!Note]  
> Wenn weder transfernorm noch transferconf im **dwCallFeatures2** -Member in [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) angegeben ist, aber linecallfeature \_ completetransf angegeben ist, ist es möglich, dass entweder funktioniert, aber der Dienstanbieter hat nicht angegeben.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2 \_ Park Direct**
</dt> <dd> <dl> <dt>



Wenn dieses Bit aktiviert ist, kann das "gesteuerte Park"-Feature mithilfe der linepark Mode- \_ Option mit [**linepark**](/windows/desktop/api/Tapi/nf-tapi-linepark)aufgerufen werden. Das linecallfeature- \_ Park Bit befindet sich auch im **dwcallfeatures** -Member.


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2 " \_ Parser"**
</dt> <dd> <dl> <dt>



Wenn dieses Bit aktiviert ist, kann die "nicht gesteuerte Park"-Funktion mithilfe der nicht gesteuerten Option linepark Mode \_ mit [**linepark**](/windows/desktop/api/Tapi/nf-tapi-linepark)aufgerufen werden. Das linecallfeature- \_ Park Bit befindet sich auch im **dwcallfeatures** -Member.

> [!Note]  
> Wenn weder Park Direct noch parknondirect im **dwCallFeatures2** -Member in [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) angegeben ist, aber linecallfeature \_ Park angegeben ist, ist es möglich, dass entweder funktioniert, aber der Dienstanbieter hat nicht angegeben.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**linecompletecall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**linecompletetransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**linepark**](/windows/desktop/api/Tapi/nf-tapi-linepark)
</dt> <dt>

[**linesetupconference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




