---
title: Zugriffsrechte Bezeichner ("f")
description: Die Windows-Filter Plattform (WFP) verwendet die standardmäßigen Win32-Zugriffsrechte sowie einen Satz WFP-spezifischer Zugriffsrechte, der in die Filter Plattform integriert ist.
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
ms.openlocfilehash: 8af182a087ade590e278bd3dd1d2bb1a64b5c598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957139"
---
# <a name="access-right-identifiers"></a>Zugriffsrechte Bezeichner

Die Windows-Filter Plattform (WFP) verwendet die [standardmäßigen Win32-Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights) sowie einen Satz WFP-spezifischer Zugriffsrechte, der in die Filter Plattform integriert ist. Diese Zugriffsrechte werden ausschließlich zum Sichern von Objekten im Benutzermodus verwendet. Kernelmodusaufrufer umgehen alle Zugriffs Überprüfungen.

Die WFP-spezifischen zugriffsrechterer Bezeichner lauten wie folgt.

<dl> <dt>

<span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**Hinzufügen von "f"- \_ actrl \_**
</dt> <dd> <dl> <dt>



Fügen Sie der Basis Filter-Engine (BFE) ein Objekt hinzu. Dieses Zugriffsrecht ist erforderlich, um [**fwpm \* Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) -Funktionen aufzurufen.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**\_ \_ Link zum Hinzufügen von "f"-actrl \_**
</dt> <dd> <dl> <dt>



Hinzufügen eines Objekts, auf das über einen Link verwiesen wird Beispielsweise wird dieses Zugriffsrecht für Aufrufe benötigt, auf die über GUIDs verwiesen wird.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**f- \_ v-actrl \_ Begin \_ Read \_**
</dt> <dd> <dl> <dt>



Beginnen Sie eine schreibgeschützte Transaktion. Dieses Zugriffsrecht ist erforderlich, um [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)aufzurufen.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**f/a- \_ \_ \_ Schreibvorgänge starten \_**
</dt> <dd> <dl> <dt>



Beginnen Sie eine Transaktion mit Lese-/Schreibzugriff. Dieses Zugriffsrecht ist erforderlich, um [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) für eine Lese-/Schreibtransaktion aufzurufen.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_kwpm-actrl- \_ Klassifizierung**
</dt> <dd> <dl> <dt>



Klassifizieren eines Remote Prozedur Aufrufs (RPC). Dieses Zugriffsrecht wird von der RPC-Laufzeit benötigt, um RPC-Filter zu erzwingen.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**WPM- \_ actrl-Aufzählung \_**
</dt> <dd> <dl> <dt>



Auflisten. Dieses Zugriffsrecht ist erforderlich, um [**fwpm \* CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) -Funktionen aufzurufen. Zum Auflisten eines Objekts benötigt der Aufrufer ebenfalls fwpm- \_ actrl- \_ Lesezugriff auf das Objekt.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**geöffnetes WPM- \_ actrl \_**
</dt> <dd> <dl> <dt>



Öffnen Sie eine Sitzung für die Filter-Engine. Dieses Zugriffsrecht ist erforderlich, um [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)aufzurufen.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**\_Lesezugriff auf die Datei \_**
</dt> <dd> <dl> <dt>



Lesen. Dieses Zugriffsrecht ist erforderlich, um [**fwpm \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) und [**fwpm \* GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) -Funktionen aufzurufen.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**Lese Statistik für das awpm- \_ actrl \_ \_**
</dt> <dd> <dl> <dt>



Lesen von Statistiken. Dieses Zugriffsrecht ist erforderlich, um [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) und [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)aufzurufen.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**Konto für die \_ Anmeldung mit dem \_ Anmelde Namen**
</dt> <dd> <dl> <dt>



Führen Sie den Schritt zum Abonnieren aus. Dieses Zugriffsrecht ist erforderlich, um [**fwpm \* SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) -Funktionen aufzurufen. Um eine Benachrichtigung für ein Objekt zu erhalten, benötigt ein Abonnent ebenfalls fwpm- \_ actrl- \_ Lesezugriff auf das Objekt.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**f- \_ \_ /Schreibzugriff**
</dt> <dd> <dl> <dt>



Schreiben von Engine-Optionen. Dieses Zugriffsrecht ist erforderlich, um [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)aufzurufen.


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**allgemeiner f- \_ \_ Lesevorgang**
</dt> <dd> <dl> <dt>



Standard \_ Rechte \_ gelesene \| f \_ & \_ \_ \_ \| \_ \_ \| \_ \_ \| \_ \_ \| \_ \_ \_ # amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; amp; quot; Lesen


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**\_Allgemeine Ausführung von "f" \_**
</dt> <dd> <dl> <dt>



Standard \_ Rechte \_ Ausführen von \| swpm \_ actrl \_ enum SS-actrl \| \_ \_ abonnieren


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**allgemeiner f- \_ \_ Schreibvorgang**
</dt> <dd> <dl> <dt>



Standard \_ Rechte Schreib Berechtigung für das Löschen von Lese-/Ausgabe-/Ausgabe-/Quell-hinzufügen \_ \| \| \_ \_ \| \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**\_alle allgemeinen voll \_ ständig**
</dt> <dd> <dl> <dt>



Standard \_ Rechte \_ erforderlich, \| f WPM- \_ actrl \_ Add \| f WPM \_ actrl \_ Add Link f/amp; \_ \| \_ actrl \_ Begin \_ Read \_ TXn \| f. \_ \_ \_ \_ \| \_ \_ klassifizieren von \| BPM- \_ actrl \_ Enum \| f- \_ actrl \_ Open \| f \_ \_ \| \_ \_ \_ \| \_ \_ \| \_ \_ -actrl lesen Sie den Befehl zum Lesen von Daten, Lese Statistik, f


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>"F"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Windows-Filter Plattform Access Control Modell](access-control.md)
</dt> <dt>

[Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

