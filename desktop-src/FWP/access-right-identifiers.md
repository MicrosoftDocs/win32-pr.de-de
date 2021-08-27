---
title: Zugriffsberechtigungsbezeichner (Fwpmu.h)
description: Windows Die Filterplattform (WFP) verwendet die Win32-Standardzugriffsrechte sowie eine Reihe von WFP-spezifischen Zugriffsrechten, die in die Filterplattform integriert sind.
ms.assetid: 77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c
topic_type:
- apiref
api_name:
- FWPM_ACTRL_ADD
- FWPM_ACTRL_ADD_LINK
- FWPM_ACTRL_BEGIN_READ_TXN
- FWPM_ACTRL_BEGIN_WRITE_TXN
- FWPM_ACTRL_CLASSIFY
- FWPM_ACTRL_ENUM
- FWPM_ACTRL_OPEN
- FWPM_ACTRL_READ
- FWPM_ACTRL_READ_STATS
- FWPM_ACTRL_SUBSCRIBE
- FWPM_ACTRL_WRITE
- FWPM_GENERIC_READ
- FWPM_GENERIC_EXECUTE
- FWPM_GENERIC_WRITE
- FWPM_GENERIC_ALL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6deee82b792f525814ac4c841da8a848e4f7b978720755c82f93a9569ba21ca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951378"
---
# <a name="access-right-identifiers"></a>Zugriffsberechtigungsbezeichner

Windows Die Filterplattform (WFP) verwendet die [Win32-Standardzugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights) sowie eine Reihe von WFP-spezifischen Zugriffsrechten, die in die Filterplattform integriert sind. Diese Zugriffsrechte werden nur zum Schützen von Objekten im Benutzermodus verwendet. Aufrufer im Kernelmodus umgehen alle Zugriffsüberprüfungen.

WFP-spezifische Zugriffsberechtigungsbezeichner lauten wie folgt.

<dl> <dt>

<span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ ADD**
</dt> <dd> <dl> <dt>



Fügen Sie der Basisfilter-Engine (BFE) ein -Objekt hinzu. Dieses Zugriffsrecht ist erforderlich, um [**Fwpm \* Add0-Funktionen aufrufen zu**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) können.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ LINK \_ HINZUFÜGEN**
</dt> <dd> <dl> <dt>



Fügen Sie ein Objekt hinzu, auf das über einen Link verwiesen wird. Dieses Zugriffsrecht ist beispielsweise für Aufrufe erforderlich, auf die über GUIDs verwiesen wird.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ BEGIN \_ READ \_ TXN**
</dt> <dd> <dl> <dt>



Startet eine schreibgeschützte Transaktion. Dieses Zugriffsrecht ist zum Aufrufen von [**FwpmTransactionBegin0 erforderlich.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ BEGIN \_ WRITE \_ TXN**
</dt> <dd> <dl> <dt>



Starten sie eine Lese-/Schreibtransaktion. Dieses Zugriffsrecht ist erforderlich, um [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) für eine Lese-/Schreibtransaktion aufrufen zu können.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM \_ ACTRL \_ CLASSIFY**
</dt> <dd> <dl> <dt>



Klassifizieren eines Remoteprozeduraufrufs (RPC). Dieses Zugriffsrecht wird von der RPC-Laufzeit benötigt, um RPC-Filter zu erzwingen.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**\_ \_ FWPM-ACTRL-ENUM**
</dt> <dd> <dl> <dt>



Auflisten. Dieses Zugriffsrecht ist erforderlich, um [**Fwpm \* CreateEnumHandle0-Funktionen aufrufen zu**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) können. Um ein Objekt aufzählen zu können, benötigt der Aufrufer auch FWPM \_ ACTRL \_ READ-Zugriff auf das Objekt.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ GEÖFFNET**
</dt> <dd> <dl> <dt>



Öffnen Sie eine Sitzung mit der Filter-Engine. Dieses Zugriffsrecht ist erforderlich, um [**FwpmEngineOpen0 aufrufen zu können.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ READ**
</dt> <dd> <dl> <dt>



Lesen. Dieses Zugriffsrecht ist erforderlich, um [**die Funktionen Fwpm \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) und [**Fwpm \* GetByKey0 aufrufen zu**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) können.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ READ \_ STATS**
</dt> <dd> <dl> <dt>



Lesen von Statistiken. Dieses Zugriffsrecht ist erforderlich, um [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) und [**IkeextGetStatistics0 aufrufen zu können.**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM \_ ACTRL \_ SUBSCRIBE**
</dt> <dd> <dl> <dt>



Führen Sie den Schritt zum Abonnieren aus. Dieses Zugriffsrecht ist zum Aufrufen von [**Fwpm \* SubscribeChanges0-Funktionen**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) erforderlich. Um eine Benachrichtigung für ein Objekt zu erhalten, benötigt ein Abonnent auch FWPM \_ ACTRL \_ READ-Zugriff auf das Objekt.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ WRITE**
</dt> <dd> <dl> <dt>



Schreib-Engine-Optionen. Dieses Zugriffsrecht ist erforderlich, um [**FwpmEngineSetOption0 aufrufen zu können.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**GENERISCHER \_ \_ FWPM-LESE-CODE**
</dt> <dd> <dl> <dt>



STANDARD \_ RIGHTS \_ READ \| FWPM \_ ACTRL \_ BEGIN \_ READ \_ TXN \| FWPM \_ ACTRL \_ CLASSIFY \| FWPM \_ ACTRL \_ OPEN \| FWPM \_ ACTRL \_ READ \| FWPM \_ ACTRL \_ READ \_ STATS


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**FWPM \_ GENERIC \_ EXECUTE**
</dt> <dd> <dl> <dt>



STANDARD \_ RIGHTS \_ EXECUTE \| FWPM \_ ACTRL \_ ENUM \| FWPM \_ ACTRL \_ SUBSCRIBE


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**GENERISCHER \_ \_ FWPM-SCHREIBZUGRIFF**
</dt> <dd> <dl> <dt>



STANDARD \_ RIGHTS \_ WRITE \| DELETE \| FWPM \_ ACTRL \_ ADD \| FWPM \_ ACTRL \_ ADD \_ LINK \| FWPM \_ ACTRL \_ BEGIN \_ WRITE \_ TXN \| FWPM \_ ACTRL \_ WRITE


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM \_ GENERIC \_ ALL**
</dt> <dd> <dl> <dt>



STANDARD \_ RIGHTS \_ REQUIRED \| FWPM \_ ACTRL \_ ADD \| FWPM \_ ACTRL \_ ADD \_ LINK \| FWPM \_ ACTRL \_ BEGIN \_ READ \_ TXN \| FWPM \_ ACTRL \_ BEGIN \_ WRITE \_ TXN \| FWPM \_ ACTRL \_ CLASSIFY \| FWPM \_ ACTRL \_ ENUM \| FWPM \_ ACTRL \_ OPEN \| FWPM \_ ACTRL \_ READ \| FWPM \_ ACTRL \_ READ \_ STATS \| FWPM \_ ACTRL \_ SUBSCRIBE \| FWPM \_ ACTRL \_ WRITE


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Windows Filtern des plattformübergreifenden Access Control Modells](access-control.md)
</dt> <dt>

[Standardzugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

