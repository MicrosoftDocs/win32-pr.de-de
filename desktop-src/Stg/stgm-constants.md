---
title: STGM-Konstanten (ObjBase.h)
description: Flags, die Bedingungen zum Erstellen und Löschen des Objekts und zugriffsmodi für das Objekt angeben.
ms.assetid: 15a35da9-332a-46e1-9190-500c95e26f59
topic_type:
- apiref
api_name:
- STGM_READ
- STGM_WRITE
- STGM_READWRITE
- STGM_SHARE_DENY_NONE
- STGM_SHARE_DENY_READ
- STGM_SHARE_DENY_WRITE
- STGM_SHARE_EXCLUSIVE
- STGM_PRIORITY
- STGM_CREATE
- STGM_CONVERT
- STGM_FAILIFTHERE
- STGM_DIRECT
- STGM_TRANSACTED
- STGM_NOSCRATCH
- STGM_NOSNAPSHOT
- STGM_SIMPLE
- STGM_DIRECT_SWMR
- STGM_DELETEONRELEASE
api_location:
- ObjBase.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18248e862c3d5981e9c34b29522b1cd75d2b61cf78a52613b3d28a1d2c98b4fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661970"
---
# <a name="stgm-constants"></a>STGM-Konstanten

Die STGM-Konstanten sind Flags, die Bedingungen zum Erstellen und Löschen des Objekts und zugriffsmodi für das Objekt angeben. Die STGM-Konstanten sind in den Schnittstellen [**IStorage,**](/windows/desktop/api/Objidl/nn-objidl-istorage) [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)und [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) sowie in den Funktionen [**StgCreateDocfile,**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) [**StgCreateStorageEx,**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) [**StgCreateDocfileOnILockBytes,**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes) [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)und [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) enthalten.

Diese Elemente werden häufig mithilfe eines **OR-Operators** kombiniert. Sie werden in Gruppen interpretiert, wie in der folgenden Tabelle aufgeführt. Es ist nicht gültig, mehr als ein Element aus einer einzelnen Gruppe zu verwenden.

Verwenden Sie beim Erstellen eines Objekts ein Flag aus der Erstellungsgruppe, z. B. mit [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) oder [**IStorage::CreateStream.**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)

Weitere Informationen zur Transaktion finden Sie im Abschnitt "Hinweise".



| Group                      | Flag                         | Wert       |
|----------------------------|------------------------------|-------------|
| Zugriff                     | **STGM \_ READ**               | 0x00000000L |
|                            | **STGM \_ WRITE**              | 0x00000001L |
|                            | **STGM \_ READWRITE**          | 0x00000002L |
| Freigabe                    | **STGM \_ SHARE \_ DENY \_ NONE**  | 0x00000040L |
|                            | **STGM \_ SHARE \_ DENY \_ READ**  | 0x00000030L |
|                            | **STGM \_ SHARE \_ DENY \_ WRITE** | 0x00000020L |
|                            | **STGM \_ SHARE \_ EXCLUSIVE**   | 0x00000010L |
|                            | **STGM \_ PRIORITY**           | 0x00040000L |
| Erstellung                   | **STGM \_ CREATE**             | 0x00001000L |
|                            | **STGM \_ CONVERT**            | 0x00020000L |
|                            | **STGM \_ FAILIFTHERE**        | 0x00000000L |
| Transaktionen             | **STGM \_ DIRECT**             | 0x00000000L |
|                            | **STGM \_ TRANSACTED**         | 0x00010000L |
| Transaktionsleistung | **STGM \_ NOSCRATCH**          | 0x00100000L |
|                            | **STGM \_ NOSNAPSHOT**         | 0x00200000L |
| Direct SWMR und Simple     | **STGM \_ SIMPLE**             | 0x08000000L |
|                            | **STGM \_ DIRECT \_ SWMR**       | 0x00400000L |
| Bei Release löschen          | **STGM \_ DELETEONRELEASE**    | 0x04000000L |



 

<dl> <dt>

<span id="STGM_READ"></span><span id="stgm_read"></span>**STGM \_ READ**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Gibt an, dass das Objekt schreibgeschützt ist, was bedeutet, dass keine Änderungen vorgenommen werden können. Wenn beispielsweise ein Streamobjekt mit **STGM \_ READ** geöffnet wird, kann die [**ISequentialStream::Read-Methode**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) aufgerufen werden, die [**ISequentialStream::Write-Methode**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) jedoch möglicherweise nicht. Wenn ein Speicherobjekt mit **STGM \_ READ** geöffnet wurde, können die Methoden [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) und [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) aufgerufen werden, die Methoden [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) und [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) jedoch möglicherweise nicht.


</dt> </dl> </dd> <dt>

<span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM \_ WRITE**
</dt> <dd> <dl> <dt>

0x00000001L
</dt> <dt>



Ermöglicht das Speichern von Änderungen am Objekt, lässt jedoch keinen Zugriff auf dessen Daten zu. Die bereitgestellten Implementierungen der Schnittstellen [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) und [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) unterstützen diesen Schreibmodus nicht.


</dt> </dl> </dd> <dt>

<span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM \_ READWRITE**
</dt> <dd> <dl> <dt>

0x00000002L
</dt> <dt>



Ermöglicht den Zugriff auf und die Änderung von Objektdaten. Wenn beispielsweise ein Streamobjekt in diesem Modus erstellt oder geöffnet wird, ist es möglich, sowohl [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) als auch **IStream::Write** aufzurufen. Beachten Sie, dass diese Konstante kein einfacher binärer **OR-Vorgang** der **STGM \_ WRITE-** und **STGM \_ READ-Elemente** ist.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM \_ SHARE \_ DENY \_ NONE**
</dt> <dd> <dl> <dt>

0x00000040L
</dt> <dt>



Gibt an, dass nachfolgenden Öffnungen des -Objekts der Lese- oder Schreibzugriff nicht verweigert wird. Wenn kein Flag aus der Freigabegruppe angegeben ist, wird dieses Flag angenommen.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM \_ SHARE \_ DENY \_ READ**
</dt> <dd> <dl> <dt>

0x00000030L
</dt> <dt>



Verhindert, dass andere Benutzer das Objekt anschließend im **STGM \_ READ-Modus** öffnen. Sie wird in der Regel für ein Stammspeicherobjekt verwendet.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM \_ SHARE \_ DENY \_ WRITE**
</dt> <dd> <dl> <dt>

0x00000020L
</dt> <dt>



Verhindert, dass andere Benutzer das Objekt anschließend für den **STGM \_ WRITE-** oder **STGM \_ READWRITE-Zugriff** öffnen. Im Transaktionsmodus kann die Freigabe von **STGM \_ SHARE \_ DENY \_ WRITE** oder **STGM \_ SHARE \_ EXCLUSIVE** die Leistung erheblich verbessern, da keine Momentaufnahmen erforderlich sind. Weitere Informationen zur Transaktion finden Sie im Abschnitt "Hinweise".


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM \_ SHARE \_ EXCLUSIVE**
</dt> <dd> <dl> <dt>

0x00000010L
</dt> <dt>



Verhindert, dass andere Benutzer das Objekt anschließend in einem beliebigen Modus öffnen. Beachten Sie, dass dieser Wert kein einfacher bitweiser **OR-Vorgang** der **WERTE STGM \_ SHARE \_ DENY \_ READ** und **STGM \_ SHARE \_ DENY \_ WRITE** ist. Im Transaktionsmodus kann die Freigabe von **STGM \_ SHARE \_ DENY \_ WRITE** oder **STGM \_ SHARE \_ EXCLUSIVE** die Leistung erheblich verbessern, da keine Momentaufnahmen erforderlich sind. Weitere Informationen zur Transaktion finden Sie im Abschnitt "Hinweise".


</dt> </dl> </dd> <dt>

<span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**STGM \_ PRIORITY**
</dt> <dd> <dl> <dt>

0x00040000L
</dt> <dt>



Öffnet das Speicherobjekt mit exklusivem Zugriff auf die zuletzt ausgeführte Version, für die ein Commit ausgeführt wurde. Daher können andere Benutzer keine Änderungen an dem Objekt committen, während es im Prioritätsmodus geöffnet ist. Sie profitieren von Leistungsvorteilen für Kopiervorgänge, verhindern jedoch, dass andere Änderungen committen. Begrenzen Sie die Zeit, in der Objekte im Prioritätsmodus geöffnet sind. Sie müssen **STGM \_ DIRECT** und **STGM \_ READ** im Prioritätsmodus angeben, und Sie können **STGM \_ DELETEONRELEASE** nicht angeben. **STGM \_ DELETEONRELEASE** ist nur beim Erstellen eines Stammobjekts gültig, z. B. mit [**StgCreateStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) Sie ist beim Öffnen eines vorhandenen Stammobjekts ungültig, z. B. mit [**StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) Sie ist auch beim Erstellen oder Öffnen eines Unterelements ungültig, z. B. mit [**IStorage::OpenStorage.**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)


</dt> </dl> </dd> <dt>

<span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM \_ CREATE**
</dt> <dd> <dl> <dt>

0x00001000L
</dt> <dt>



Gibt an, dass ein vorhandenes Speicherobjekt oder ein vorhandener Stream entfernt werden soll, bevor es durch das neue Objekt ersetzt wird. Ein neues -Objekt wird erstellt, wenn dieses Flag nur angegeben wird, wenn das vorhandene Objekt erfolgreich entfernt wurde.

Dieses Flag wird beim Erstellen von verwendet:

-   Ein Speicherobjekt auf einem Datenträger, aber eine Datei mit diesem Namen ist vorhanden.
-   Ein Objekt in einem Speicherobjekt, aber ein Objekt mit dem angegebenen Namen ist vorhanden.
-   Ein Bytearrayobjekt, aber es ist ein Objekt mit dem angegebenen Namen vorhanden.

Dieses Flag kann nicht mit offenen Vorgängen wie [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) oder [**IStorage::OpenStream verwendet werden.**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)


</dt> </dl> </dd> <dt>

<span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM \_ CONVERT**
</dt> <dd> <dl> <dt>

0x00020000L
</dt> <dt>



Erstellt das neue -Objekt unter Beibehaltung vorhandener Daten in einem Stream mit dem Namen "Contents". Im Fall eines Speicherobjekts oder bytearrays werden die alten Daten in einen Stream formatiert, unabhängig davon, ob die vorhandene Datei oder das Bytearray derzeit ein mehrschichtiges Speicherobjekt enthält. Dieses Flag kann nur beim Erstellen eines Stammspeicherobjekts verwendet werden. Sie kann nicht innerhalb eines Speicherobjekts verwendet werden. Beispiel: in [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream). Es ist auch nicht zulässig, dieses Flag und das **STGM \_ DELETEONRELEASE-Flag** gleichzeitig zu verwenden.


</dt> </dl> </dd> <dt>

<span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM \_ FAILIFTHERE**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Bewirkt, dass der Erstellungsvorgang fehlschlägt, wenn ein vorhandenes Objekt mit dem angegebenen Namen vorhanden ist. In diesem Fall wird **STG \_ E \_ FILEALREADYEXISTS** zurückgegeben. Dies ist der Standarderstellungsmodus. Das heißt, wenn kein anderes Erstellungsflag angegeben ist, **wird STGM \_ FAILIFTHERE** impliziert.


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM \_ DIRECT**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Gibt an, dass jede Änderung an einem Speicher- oder Streamelement im direkten Modus geschrieben wird, während sie auftritt. Dies ist die Standardeinstellung, wenn **weder STGM \_ DIRECT** noch **STGM \_ TRANSACTED** angegeben ist.


</dt> </dl> </dd> <dt>

<span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM \_ TRANSACTED**
</dt> <dd> <dl> <dt>

0x00010000L
</dt> <dt>



Gibt an, dass Änderungen im Transaktionsmodus nur gepuffert und geschrieben werden, wenn ein expliziter Commitvorgang aufgerufen wird. Um die Änderungen zu ignorieren, rufen Sie die [**Revert-Methode**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) in der [**IStream-,**](/windows/desktop/api/Objidl/nn-objidl-istream) [**IStorage-**](/windows/desktop/api/Objidl/nn-objidl-istorage)oder [**IPropertyStorage-Schnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) auf. Die COM-Verbunddateiimplementierung von **IStorage** unterstützt keine transaktiven Datenströme. Das bedeutet, dass Streams nur im direkten Modus geöffnet werden können, und Sie können keine Änderungen daran rückgängig machen, aber transaktionsverwendete Speicher werden unterstützt. Die Verbunddatei-, eigenständigen und NTFS-Dateisystemimplementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) unterstützen ebenfalls keine transaktiven, einfachen Eigenschaftensätze, da diese Eigenschaftensätze in Streams gespeichert werden. Transaktionen von nicht einfachen Eigenschaftensätzen, die durch Angabe des **PROPSETFLAG \_ NONSIMPLE-Flags** im *grfFlags-Parameter* von [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)erstellt werden können, werden jedoch unterstützt.


</dt> </dl> </dd> <dt>

<span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM \_ NOSCRATCH**
</dt> <dd> <dl> <dt>

0x00100000L
</dt> <dt>



Gibt an, dass im Transaktionsmodus in der Regel eine temporäre Scratchdatei verwendet wird, um Änderungen zu speichern, bis die **Commit-Methode** aufgerufen wird. Wenn **Sie STGM \_ NOSCRATCH** angeben, kann der nicht verwendete Teil der ursprünglichen Datei als Arbeitsraum verwendet werden, anstatt zu diesem Zweck eine neue Datei zu erstellen. Dies wirkt sich nicht auf die Daten in der ursprünglichen Datei aus und kann in bestimmten Fällen zu einer verbesserten Leistung führen. Es ist nicht zulässig, dieses Flag anzugeben, ohne **auch STGM \_ TRANSACTED** anzugeben, und dieses Flag darf nur in einem geöffneten Stamm verwendet werden. Weitere Informationen zum NoScratch-Modus finden Sie im Abschnitt "Hinweise".


</dt> </dl> </dd> <dt>

<span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM \_ NOSNAPSHOT**
</dt> <dd> <dl> <dt>

0x00200000L
</dt> <dt>



Dieses Flag wird verwendet, wenn ein Speicherobjekt mit **STGM \_ TRANSACTED** und ohne **STGM \_ SHARE \_ EXCLUSIVE** oder **STGM \_ SHARE \_ DENY WRITE geöffnet \_ wird.** In diesem Fall verhindert die Angabe **von STGM \_ NOSNAPSHOT,** dass die vom System bereitgestellte Implementierung eine Momentaufnahmekopie der Datei erstellt. Stattdessen werden Änderungen an der Datei an das Ende der Datei geschrieben. Nicht verwendeter Speicherplatz wird nur dann wieder freigefordert, wenn während des Commits eine Konsolidierung durchgeführt wird und nur ein aktueller Writer in der Datei vor sich geht. Wenn die Datei ohne Momentaufnahmemodus geöffnet wird, kann kein weiterer Geöffnetvorgang ohne Angabe von **STGM \_ NOSNAPSHOT ausgeführt werden.** Dieses Flag kann nur in einem Root-Open-Vorgang verwendet werden. Weitere Informationen zum NoSnapshot-Modus finden Sie im Abschnitt "Hinweise".


</dt> </dl> </dd> <dt>

<span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM \_ SIMPLE**
</dt> <dd> <dl> <dt>

0x08000000L
</dt> <dt>



Ermöglicht eine schnellere Implementierung einer Verbunddatei in einem begrenzten, aber häufig verwendeten Fall. Weitere Informationen finden Sie im Abschnitt "Hinweise".


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM \_ DIRECT \_ SWMR**
</dt> <dd> <dl> <dt>

0x00400000L
</dt> <dt>



Unterstützt den direkten Modus für Dateivorgänge mit einzelnem Writer und mehrerenReadern. Weitere Informationen finden Sie im Abschnitt "Hinweise".


</dt> </dl> </dd> <dt>

<span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM \_ DELETEONRELEASE**
</dt> <dd> <dl> <dt>

0x04000000L
</dt> <dt>



Gibt an, dass die zugrunde liegende Datei automatisch zerstört werden soll, wenn das Stammspeicherobjekt freigegeben wird. Diese Funktion ist am nützlichsten zum Erstellen temporärer Dateien. Dieses Flag kann nur beim Erstellen eines Stammobjekts verwendet werden, z. B. mit [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Er ist ungültig, wenn ein Stammobjekt geöffnet wird, z. B. mit [**StgOpenStorageEx,**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)oder wenn ein Unterelement erstellt oder geöffnet wird, z. B. mit [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream). Es ist auch nicht zulässig, dieses Flag und das STGM \_ CONVERT-Flag gleichzeitig zu verwenden.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können diese Flags kombinieren, aber Sie können nur ein Flag aus jeder Gruppe verwandter Flags auswählen. In der Regel muss für alle Funktionen und Methoden, die diese Konstanten verwenden, ein Flag aus jeder Zugriffs- und Freigabegruppe angegeben werden. Flags aus anderen Gruppen sind optional.

### <a name="transacted-mode"></a>Transaktionsmodus

Wenn das **FLAG STGM \_ DIRECT** angegeben wird, kann nur eines der folgenden Flagkombinationen aus den Zugriffs- und Freigabegruppen angegeben werden.

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

Beachten Sie, dass der direkte Modus durch das Fehlen von **STGM \_ TRANSACTED impliziert wird.** Wenn also weder **STGM \_ DIRECT** noch **STGM \_ TRANSACTED angegeben** ist, wird **STGM \_ DIRECT** angenommen.

Wenn das **STGM-TransactED-Flag \_** angegeben wird, werden Objekte im Transaktionsmodus erstellt oder geöffnet. In diesem Modus werden Änderungen an einem Objekt erst beibehalten, wenn ein Committed ausgeführt wurde. Beispielsweise werden Änderungen an einem transaktionsorientierten Speicherobjekt erst beibehalten, wenn die [**IStorage::Commit-Methode**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) aufgerufen wird. Änderungen an einem solchen Speicherobjekt gehen verloren, wenn das Speicherobjekt freigegeben wird (endgültiges Release), bevor die **Commit-Methode** aufgerufen wird, oder wenn die [**IStorage::Revert-Methode**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) aufgerufen wird.

Wenn ein Objekt im transaktionsorientierten Modus erstellt oder geöffnet wird, muss die Implementierung sowohl die ursprünglichen Daten als auch die Aktualisierungen dieser Daten behalten, damit Updates bei Bedarf rückgängig machen können. Dies erfolgt in der Regel durch Das Schreiben von Änderungen in einen Scratchbereich, bis ein Committed ausgeführt wird, oder durch Erstellen einer Kopie der zuletzt ausgeführten Daten, die als Momentaufnahme bezeichnet wird.

Wenn ein Stammspeicherobjekt im Transaktionsmodus geöffnet wird, können Speicherort und Verhalten der Scratchdaten und momentaufnahmekopien gesteuert werden, um die Leistung mit den **FLAGs STGM \_ NOSCRATCH** und **STGM \_ NOSNAPSHOT** zu optimieren. (Ein Stammspeicherobjekt wird beispielsweise von der [**StgOpenStorageEx-Funktion**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) erhalten. Ein von der [**IStorage::OpenStorage-Methode**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) erhaltenes Speicherobjekt ist ein Unterspeicherobjekt.) In der Regel werden die Scratchdaten und Momentaufnahmen getrennt vom Speicher in temporären Dateien gespeichert.

Die Auswirkung dieser Flags hängt von der Anzahl der Leser und/oder Writer ab, die auf den Stammspeicher zugreifen.

Im Fall von "Single Writer" wird ein Speicherobjekt im Transaktionsmodus für den Schreibzugriff geöffnet, und es kann kein anderer Zugriff auf die Datei möglich sein. Das heißt, die Datei wird mit **STGM \_ TRANSACTED,** dem Zugriff auf **STGM \_ WRITE** oder **STGM \_ READWRITE** und der Freigabe von **STGM \_ SHARE EXCLUSIVE \_ geöffnet.** In diesem Fall werden Änderungen am Speicherobjekt in den Ablagebereich geschrieben. Wenn für diese Änderungen ein Committed vorgenommen wird, werden sie in den ursprünglichen Speicher kopiert. Wenn also keine Änderungen am Speicherobjekt vorgenommen werden, erfolgt keine unnötige Datenübertragung.

Im Fall von "multiple-writer" wird ein transaktives Speicherobjekt für den Schreibzugriff geöffnet, aber in freigegeben, um anderen Writern zu erlauben. Das heißt, das Speicherobjekt wird mit **STGM \_ TRANSACTED,** dem Zugriff auf **STGM \_ WRITE** oder **STGM \_ READWRITE** und der Freigabe von **STGM \_ SHARE \_ DENY \_ READ geöffnet.** Wenn stattdessen die Freigabe von **STGM \_ SHARE \_ DENY \_ NONE** angegeben wird, ist der Fall "multiple-writer, multiple-reader". In diesen Fällen wird während des Öffnens eine Momentaufnahme der ursprünglichen Daten erstellt. Daher ist auch dann eine Datenübertragung während des Öffnens erforderlich, wenn tatsächlich keine Änderungen am Speicher vorgenommen und/oder nicht von einem anderen Writer gleichzeitig geöffnet werden. Als Ergebnis kann die beste Open-Time-Leistung erzielt werden, indem das Speicherobjekt in **den Modi STGM \_ SHARE \_ DENY \_ WRITE** oder **STGM \_ SHARE EXCLUSIVE \_ geöffnet** wird. Weitere Informationen zum Commit von Änderungen bei mehreren Writern finden Sie unter [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).

Im Fall von "single-writer, multiple-reader" wird ein transaktives Speicherobjekt für den Schreibzugriff geöffnet, aber für Leser freigegeben. Das heißt, das Speicherobjekt wird vom Writer mit **STGM \_ TRANSACTED,** dem Zugriff auf **STGM \_ READWRITE** oder **STGM \_ WRITE** und der Freigabe von **STGM \_ SHARE \_ DENY \_ WRITE geöffnet.** Der Speicher wird von Lesern mit **STGM \_ TRANSACTED,** Zugriff auf **STGM \_ READ** und Freigabe von **STGM \_ SHARE \_ DENY \_ NONE geöffnet.** In diesem Fall verwendet der Writer den Scratchbereich, um Nichtcommitted-Änderungen zu speichern. Wie in den obigen Fällen kommt es beim Reader zu einer Leistungssentität bei der Offenen Zeit, während eine Momentaufnahmekopie der Daten erstellt wird.

In der Regel handelt es sich bei dem Scratchbereich um eine temporäre Datei, die von den ursprünglichen Daten getrennt ist. Wenn änderungen an der ursprünglichen Datei übergeben werden, müssen die Daten aus der temporären Datei übertragen werden. Um diese Datenübertragung zu vermeiden, kann **das STGM \_ NOSCRATCH-Flag** angegeben werden. Wenn dieses Flag angegeben wird, werden Teile der Speicherobjektdatei für den Ablagebereich anstelle einer separaten temporären Datei verwendet. Daher kann das Committen von Änderungen schnell durchgeführt werden, da nur wenig Datenübertragung erforderlich ist. Der Nachteil ist, dass die Speicherdatei größer werden kann, als sie andernfalls wäre, da sie so vergrößert werden muss, dass sie sowohl für die ursprünglichen Daten als auch für den Ablagebereich groß genug ist. Um die Daten zu konsolidieren und diesen unnötigen Bereich zu entfernen, öffnen Sie den Stammspeicher im Transaktionsmodus erneut, aber ohne das **STGM \_ NOSCRATCH-Flag zu** setzen. Rufen Sie dann [**IStorage::Commit auf,**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) und legen Sie das **FLAG STGC \_ CONSOLIDATE** fest.

Der Momentaufnahmebereich ist wie der Scratchbereich in der Regel auch eine temporäre Datei. Dies kann auch durch ein STGM-Flag beeinträchtigt werden. Durch Angabe des **STGM \_ NOSNAPSHOT-Flags** wird keine separate temporäre Momentaufnahmedatei erstellt. Stattdessen werden die ursprünglichen Daten nie geändert, auch wenn es mindestens einen Writer pro Objekt gibt. Wenn ein Committed für Änderungen vorgenommen wird, werden sie der Datei hinzugefügt, die ursprünglichen Daten bleiben jedoch intakt. Dieser Modus erhöht die Effizienz, da er die Laufzeit reduziert, da während des Öffnens keine Momentaufnahme erstellt werden muss. Die Verwendung dieses Modus kann jedoch zu einer sehr großen Speicherdatei führen, da daten in der Datei nie überschrieben werden können. Dies ist keine Beschränkung für die Größe von Dateien, die im NoSnapshot-Modus geöffnet werden.

### <a name="direct-single-writer-multiple-reader-mode"></a>Direct Single Writer, Multiple-Reader Modus

Wie beschrieben, ist es möglich, einen einzelnen Writer und mehrere Reader eines Speicherobjekts zu verwenden, wenn dieses Objekt im Transaktionsmodus geöffnet wird. Es ist auch möglich, die Einzelwriter-Multireader-Schreibweise im direkten Modus zu erreichen, indem das **STGM \_ DIRECT \_ SWMR-Flag angegeben** wird.

Im **STGM \_ DIRECT \_ SWMR-Modus** ist es möglich, dass ein Aufrufer ein Objekt für den Lese-/Schreibzugriff öffnet, während andere Aufrufer gleichzeitig die Datei für den schreibgeschützten Zugriff geöffnet haben. Es ist nicht zulässig, dieses Flag in Kombination mit dem **STGM \_ TRANSACTED-Flag zu** verwenden. In diesem Modus öffnet der Writer das -Objekt mit den folgenden Flags:

**STGM \_ DIRECT \_ SWMR** \| **STGM \_ READWRITE** \| **STGM \_ SHARE \_ DENYWRITE**

und jeder der Reader öffnet das -Objekt mit den folgenden Flags:

**STGM \_ DIRECT \_ SWMR** \| **STGM \_ READ** \| **STGM \_ SHARE \_ DENY \_ NONE**

In diesem Modus muss der Writer exklusiven Zugriff auf das Objekt erhalten, um das Speicherobjekt zu ändern. Dies ist möglich, wenn sie von allen Lesern geschlossen wurde. Der Writer verwendet die [**IDirectWriterLock-Schnittstelle,**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) um diesen exklusiven Zugriff zu erhalten.

### <a name="simple-mode"></a>Einfacher Modus

Der einfache Modus (**STGM \_ SIMPLE**) ist nützlich für Anwendungen, die vollständige Speichervorgänge ausführen. Sie ist effizient, hat jedoch die folgenden Einschränkungen:

-   Es gibt keine Unterstützung für Unterstorages.
-   Das Speicherobjekt und die daraus erhaltenen Streamobjekte können nicht gemarshallt werden.
-   Jeder Stream hat eine Mindestgröße. Wenn weniger als die minimalen Bytes in einen Stream geschrieben werden, wenn der Stream freigegeben wird, wird der Stream auf die Mindestgröße erweitert. Die Mindestgröße für eine bestimmte [**IStream-Implementierung**](/windows/desktop/api/Objidl/nn-objidl-istream) beträgt beispielsweise 4 KB. Ein Stream wird erstellt, und 1 KB wird in ihn geschrieben. Bei der endgültigen Version dieses **IStreams** wird die Streamgröße automatisch auf 4 KB erweitert. Wenn Sie anschließend den Stream öffnen und die [**IStream::Stat-Methode**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) aufrufen, wird eine Größe von 4 KB gezeigt.
-   Nicht alle Methoden von [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) oder [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) werden von der Implementierung unterstützt. Weitere Informationen finden Sie unter [IStorage – Verbunddateiimplementierung](istorage-compound-file-implementation.md)und [IStream – Verbunddateiimplementierung.](istream-compound-file-implementation.md)

[Marshalling ist](/windows/desktop/Midl/marshaling-ole-data-types) der Prozess des Packens, Entpackens und Sendens von Schnittstellenmethode-Parametern über Thread- oder Prozessgrenzen hinweg innerhalb eines Remoteprozeduraufrufs (REMOTE Procedure Call, RPC). Weitere Informationen finden Sie unter [Marshallingdetails und](../com/marshaling-details.md) [Schnittstellen-Marshalling.](../com/interface-marshaling.md)

Wenn ein Speicherobjekt durch einen Erstellungsvorgang im einfachen Modus erhalten wird:

-   Streamelemente können erstellt, aber nicht geöffnet werden.
-   Wenn ein Streamelement durch Aufrufen von [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)erstellt wird, ist es nicht möglich, einen weiteren Stream zu erstellen, bis dieses Streamobjekt freigegeben wird.
-   Nachdem alle Datenströme geschrieben wurden, rufen Sie [**IStorage::Commit auf,**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) um die Änderungen zu leeren.

Wenn ein Speicherobjekt durch einen Open-Vorgang im einfachen Modus erhalten wird:

-   Es ist möglich, immer nur ein Streamelement gleichzeitig zu öffnen.
-   Es ist nicht möglich, die Größe eines Streams durch Aufrufen der [**IStream::SetSize-Methode**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) oder durch Suchen oder Schreiben über das Ende des Streams hinaus zu ändern. Da jedoch alle Streams eine Mindestgröße haben, ist es möglich, den Stream bis zu dieser Größe zu verwenden, auch wenn ursprünglich weniger Daten in den Stream geschrieben wurden. Verwenden Sie die [**IStream::Stat-Methode,**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) um die Größe eines Streams zu bestimmen.

Beachten Sie, dass es nicht möglich ist, dieses Speicherelement im einfachen Modus zu öffnen, wenn ein Speicherelement von einem Speicherobjekt geändert wird, das sich nicht im einfachen Modus befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>ObjBase.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dt>

[**Istorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
</dt> <dt>

[**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> <dt>

[**StgOpenStorageOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
</dt> </dl>

 

