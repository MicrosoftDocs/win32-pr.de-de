---
description: Die LINECALLFEATURE2-Konstanten listen die zusätzlichen Features auf, die für \_ Konferenz-, Übertragungs- und Parkanrufe verfügbar sind.
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: LINECALLFEATURE2_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b1ef95c5427c70455466fdc4e44424a8d7bc92f768698bd3356f28256b4dbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003138"
---
# <a name="linecallfeature2_-constants"></a>LINECALLFEATURE2-Konstanten \_

Die **\_ LINECALLFEATURE2-Konstanten** listen die zusätzlichen Features auf, die für Konferenz-, Übertragungs- und Parkanrufe verfügbar sind.

<dl> <dt>

<span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2 \_ COMPLCALLBACK**
</dt> <dd> <dl> <dt>



Wenn dieses Bit ein on ist, kann das Feature "callback" mithilfe der LINECOMPLMODE CALLBACK-Option mit \_ [**lineCompleteCall aufgerufen werden.**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) Das LINECALLFEATURE \_ COMPLETECALL-Bit ist auch im **dwCallFeatures-Member** ein.


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2 \_ COMPLCAMPON**
</dt> <dd> <dl> <dt>



Wenn dieses Bit auf "on" festgelegt ist, kann das Feature "wird ein" aufgerufen werden, indem die LINECOMPLMODE-OPTION \_ MIT [**lineCompleteCall verwendet wird.**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) Das LINECALLFEATURE \_ COMPLETECALL-Bit ist auch im **dwCallFeatures-Member** ein.


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2 \_ COMPLINTRUDE**
</dt> <dd> <dl> <dt>



Wenn dieses Bit ein on ist, kann das Feature "intrude" mithilfe der LINECOMPLMODE \_ INTRUDE-Option mit [**lineCompleteCall aufgerufen werden.**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) Das LINECALLFEATURE \_ COMPLETECALL-Bit ist auch im **dwCallFeatures-Member** ein.


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2 \_ COMPLMESSAGE**
</dt> <dd> <dl> <dt>



Wenn dieses Bit ein on ist, kann das Feature "leave message" mithilfe der LINECOMPLMODE MESSAGE-Option mit \_ [**lineCompleteCall aufgerufen werden.**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) Das LINECALLFEATURE \_ COMPLETECALL-Bit ist auch im **dwCallFeatures-Member** ein.


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2 \_ NOHOLDCONFERENCE**
</dt> <dd> <dl> <dt>



Wenn dieses Bit ein on ist, kann eine "No Hold Conference" erstellt werden, indem die LINECALLPARAMFLAGS \_ NOHOLDCONFERENCE-Option mit [**lineSetupConference verwendet wird.**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) Das LINECALLFEATURE \_ SETUPCONF-Bit ist auch im **dwCallFeatures-Member** ein.


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2 \_ ONESTEPTRANSFER**
</dt> <dd> <dl> <dt>



Wenn dieses Bit ein on ist, kann "one step transfer" mithilfe der LINECALLPARAMFLAGS \_ ONESTEPTRANSFER-Option mit [**lineSetupTransfer erstellt werden.**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer) Das LINECALLFEATURE \_ SETUPTRANSFER-Bit ist auch im **dwCallFeatures-Member** ein.

> [!Note]  
> Wenn keines der "COMPL"-Bits im **dwCallFeatures2-Member** in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) angegeben ist, aber LINECALLFEATURE COMPLETECALL angegeben ist, ist es möglich, dass eines der Bits funktioniert, aber der Dienstanbieter hat nicht angegeben, welche. \_

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2 \_ TRANSFERCONF**
</dt> <dd> <dl> <dt>



Wenn dieses Bit ein on ist, kann die [**lineCompleteTransfer-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) verwendet werden, um die Übertragung als Drei-Wege-Konferenz aufzulösen. Das LINECALLFEATURE \_ COMPLETETRANSF-Bit ist auch im **dwCallFeatures-Member** ein.


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2 \_ TRANSFERNORM**
</dt> <dd> <dl> <dt>



Wenn dieses Bit ein on ist, kann die [**lineCompleteTransfer-Funktion**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) verwendet werden, um die Übertragung als normale Übertragung aufzulösen. Das LINECALLFEATURE \_ COMPLETETRANSF-Bit ist auch im **dwCallFeatures-Member** ein.

> [!Note]  
> Wenn weder TRANSFERNORM noch TRANSFERCONF im **dwCallFeatures2-Member** in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) angegeben ist, aber LINECALLFEATURE COMPLETETRANSF angegeben ist, ist es möglich, dass beides funktioniert, aber der Dienstanbieter hat nicht angegeben, welche. \_

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2 \_ PARKDIRECT**
</dt> <dd> <dl> <dt>



Wenn dieses Bit ein on ist, kann das Feature "directed park" mithilfe der LINEPARKMODE DIRECTED-Option mit \_ [**linePark aufgerufen werden.**](/windows/desktop/api/Tapi/nf-tapi-linepark) Das LINECALLFEATURE \_ PARK-Bit ist auch im **dwCallFeatures-Member** ein.


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2 \_ PARKNONDIRECT**
</dt> <dd> <dl> <dt>



Wenn dieses Bit auf "On" festgelegt ist, kann das Feature "Nicht gerichteter Park" mithilfe der LINEPARKMODE \_ NONDIRECTED-Option mit [**linePark aufgerufen werden.**](/windows/desktop/api/Tapi/nf-tapi-linepark) Das LINECALLFEATURE \_ PARK-Bit ist auch im **dwCallFeatures-Member** ein.

> [!Note]  
> Wenn weder PARKDIRECT noch PARKNONDIRECT im **dwCallFeatures2-Member** in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) angegeben ist, aber LINECALLFEATURE PARK angegeben ist, ist es möglich, dass beides funktioniert, aber der Dienstanbieter hat nicht angegeben, welche. \_

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark)
</dt> <dt>

[**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




