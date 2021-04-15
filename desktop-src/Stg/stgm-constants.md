---
title: STGM-Konstanten (objbase. h)
description: Flags, die Bedingungen für das Erstellen und Löschen des Objekts und der Zugriffs Modi für das Objekt angeben.
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
ms.openlocfilehash: cd283c2dfeddc48b6bd12f8317ec352cb62e4973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475480"
---
# <a name="stgm-constants"></a>STGM-Konstanten

Die STGM-Konstanten sind Flags, die die Bedingungen für das Erstellen und Löschen des Objekts und der Zugriffs Modi für das Objekt angeben. Die STGM-Konstanten sind in den [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)-, [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)-und [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstellen und in den Funktionen " [**stgforatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)", " [**stgfoatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)", "stgforatedocfileonilockbytes", " [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)" und " [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) " enthalten. [](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)

Diese Elemente werden häufig mit einem **or**-Operator kombiniert. Sie werden in Gruppen wie in der folgenden Tabelle aufgeführt interpretiert. Es ist nicht zulässig, mehr als ein Element aus einer einzelnen Gruppe zu verwenden.

Verwenden Sie ein Flag aus der Erstellungs Gruppe, wenn Sie ein Objekt erstellen, z. b. mit [**stgkreatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) oder [**IStorage:: foratestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).

Weitere Informationen zum Transaktions Satz finden Sie im Abschnitt "Hinweise".



| Gruppieren                      | Flag                         | Wert       |
|----------------------------|------------------------------|-------------|
| Access                     | **STGM- \_ Lesevorgang**               | 0x00000000L |
|                            | **STGM- \_ Schreibvorgang**              | 0x00000001L |
|                            | **STGM- \_ Lesevorgang**          | 0x00000002L |
| Freigabe                    | **STGM- \_ Freigabe \_ Deny " \_ None"**  | 0x00000040l |
|                            | **STGM- \_ Freigabe \_ verweigern \_ Lesen**  | 0x00000030l |
|                            | **STGM- \_ Freigabe \_ verweigern \_ schreiben** | 0x00000020l |
|                            | **STGM- \_ Freigabe \_ exklusiv**   | 0x00000010L |
|                            | **STGM- \_ Priorität**           | 0x00040000l |
| Erstellung                   | **STGM \_ Erstellen**             | 0x00001000l |
|                            | **STGM \_ konvertieren**            | 0x00020000l |
|                            | **STGM \_ FailIf**        | 0x00000000L |
| Wird transakiert             | **STGM \_ direkt**             | 0x00000000L |
|                            | **STGM \_ transaktiv**         | 0x00010000l |
| Transaktionsleistung | **STGM \_ noscratch**          | 0x00100000l |
|                            | **STGM- \_ nosnapshot**         | 0x00200000l |
| Direkte austauschen und einfache     | **STGM \_ Simple**             | 0x08000000l |
|                            | **STGM \_ Direct- \_ Austausch**       | 0x00400000l |
| Beim Release löschen          | **STGM \_ deleteonrelease**    | 0x04000000l |



 

<dl> <dt>

<span id="STGM_READ"></span><span id="stgm_read"></span>**STGM- \_ Lesevorgang**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Gibt an, dass das Objekt schreibgeschützt ist, was bedeutet, dass keine Änderungen vorgenommen werden können. Wenn z. b. ein Stream-Objekt mit **STGM- \_ Lese** Vorgang geöffnet wird, kann die [**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) -Methode aufgerufen werden, die [**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) -Methode jedoch nicht. Ebenso kann, wenn ein Speicher Objekt, das mit **STGM- \_ Lese** Vorgang geöffnet wurde, die [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) -und [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) -Methode aufgerufen werden, aber die [**IStorage:: foatestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) -Methode und die [**IStorage:: foratestorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) -Methode.


</dt> </dl> </dd> <dt>

<span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM- \_ Schreibvorgang**
</dt> <dd> <dl> <dt>

0x00000001L
</dt> <dt>



Ermöglicht das Speichern von Änderungen am-Objekt, aber nicht den Zugriff auf seine Daten. Der schreibgeschützte Modus wird von den bereitgestellten Implementierungen der [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle und der [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM- \_ Lesevorgang**
</dt> <dd> <dl> <dt>

0x00000002L
</dt> <dt>



Ermöglicht den Zugriff und die Änderung von Objektdaten. Wenn z. b. ein Stream-Objekt in diesem Modus erstellt oder geöffnet wird, ist es möglich, sowohl [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) als auch **IStream:: Write** aufzurufen. Beachten Sie, dass diese Konstante keine einfache Binärdatei **oder** Operation der Read-und **STGM- \_ Lese** Elemente von **STGM \_** ist.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM- \_ Freigabe \_ Deny " \_ None"**
</dt> <dd> <dl> <dt>

0x00000040l
</dt> <dt>



Gibt an, dass nachfolgende Öffnungen des Objekts keinen Lese-oder Schreibzugriff verweigert werden. Wenn kein Flag aus der Freigabe Gruppe angegeben wird, wird dieses Flag angenommen.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM- \_ Freigabe \_ verweigern \_ Lesen**
</dt> <dd> <dl> <dt>

0x00000030l
</dt> <dt>



Verhindert, dass andere das Objekt später im **STGM- \_ Lesemodus** öffnen. Sie wird in der Regel für ein Stamm Speicher Objekt verwendet.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM- \_ Freigabe \_ verweigern \_ schreiben**
</dt> <dd> <dl> <dt>

0x00000020l
</dt> <dt>



Verhindert, dass andere das Objekt später für den Zugriff auf **STGM- \_ Schreib** -oder **STGM- \_ Lese** Vorgänge öffnen. Im transaktiven Modus kann die Freigabe von " **STGM-Freigabe \_ \_ verweigern \_** " oder " **STGM \_ Freigabe \_ exklusiv** " die Leistung erheblich verbessern, da keine Momentaufnahmen erforderlich sind. Weitere Informationen zum Transaktions Satz finden Sie im Abschnitt "Hinweise".


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM- \_ Freigabe \_ exklusiv**
</dt> <dd> <dl> <dt>

0x00000010L
</dt> <dt>



Verhindert, dass andere das Objekt später in einem beliebigen Modus öffnen. Beachten Sie, dass es sich bei diesem Wert nicht um eine einfache bitweise **or** -Operation der **STGM- \_ Freigabe \_ deny- \_ Lese** -und **STGM-Freigabe- \_ \_ \_ Schreib** Werte handelt. Im transaktiven Modus kann die Freigabe von " **STGM-Freigabe \_ \_ verweigern \_** " oder " **STGM \_ Freigabe \_ exklusiv** " die Leistung erheblich verbessern, da keine Momentaufnahmen erforderlich sind. Weitere Informationen zum Transaktions Satz finden Sie im Abschnitt "Hinweise".


</dt> </dl> </dd> <dt>

<span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**STGM- \_ Priorität**
</dt> <dd> <dl> <dt>

0x00040000l
</dt> <dt>



Öffnet das Speicher Objekt mit exklusivem Zugriff auf die zuletzt zugesicherte Version. Folglich können andere Benutzer keine Änderungen an dem Objekt übertragen, während Sie es im Prioritäts Modus geöffnet haben. Sie profitieren von Leistungsvorteilen bei Kopier Vorgängen, aber Sie verhindern, dass andere Änderungen an Änderungen vornehmen. Beschränken Sie den Zeitraum, in dem Objekte im Prioritäts Modus geöffnet werden. Sie müssen **STGM \_ Direct** und STGM mit dem Prioritäts Modus **\_ Lesen** angeben, und Sie können **STGM \_ deleteonrelease** nicht angeben. **STGM \_ Deleteonrelease** ist nur gültig, wenn ein Stamm Objekt erstellt wird, z. b. mit [**stgkreatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Dies ist nicht zulässig, wenn ein vorhandenes Stamm Objekt geöffnet wird, z. b. mit [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex). Dies ist auch beim Erstellen oder Öffnen eines untergeordneten Elements (z. b. bei [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)) nicht gültig.


</dt> </dl> </dd> <dt>

<span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM \_ Erstellen**
</dt> <dd> <dl> <dt>

0x00001000l
</dt> <dt>



Gibt an, dass ein vorhandenes Speicher Objekt oder ein vorhandener Stream entfernt werden soll, bevor das neue Objekt es ersetzt. Ein neues-Objekt wird erstellt, wenn dieses Flag nur angegeben wird, wenn das vorhandene Objekt erfolgreich entfernt wurde.

Dieses Flag wird verwendet, wenn versucht wird, Folgendes zu erstellen:

-   Ein Speicher Objekt auf einem Datenträger, aber eine Datei mit diesem Namen ist vorhanden.
-   Ein Objekt in einem Speicher Objekt, aber es ist ein Objekt mit dem angegebenen Namen vorhanden.
-   Ein Bytearray-Objekt, aber eine mit dem angegebenen Namen ist vorhanden.

Dieses Flag kann nicht mit offenen Vorgängen verwendet werden, wie z. b. [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) oder [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).


</dt> </dl> </dd> <dt>

<span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM \_ konvertieren**
</dt> <dd> <dl> <dt>

0x00020000l
</dt> <dt>



Erstellt das neue-Objekt, während vorhandene Daten in einem Stream mit dem Namen "Content" beibehalten werden. Bei einem Speicher Objekt oder einem Bytearray werden die alten Daten in einen Stream formatiert, unabhängig davon, ob die vorhandene Datei oder das Bytearray derzeit ein mehrschichtiges Speicher Objekt enthält. Dieses Flag kann nur beim Erstellen eines Stamm Speicher Objekts verwendet werden. Sie kann nicht innerhalb eines Speicher Objekts verwendet werden. beispielsweise in [**IStorage:: foratestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream). Es ist auch ungültig, dieses Flag und das **STGM \_ deleteonrelease** -Flag gleichzeitig zu verwenden.


</dt> </dl> </dd> <dt>

<span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM \_ FailIf**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Bewirkt, dass der Erstellungs Vorgang fehlschlägt, wenn ein vorhandenes Objekt mit dem angegebenen Namen vorhanden ist. In diesem Fall wird **STG \_ E \_ filealleseryist** zurückgegeben. Dies ist der Standard Erstellungs Modus. Das heißt, wenn kein anderes Create-Flag angegeben ist, wird **STGM \_ failisthere** impliziert.


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM \_ direkt**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Gibt an, dass im direkten Modus jede Änderung an einem Speicher-oder streamelement geschrieben wird, wenn es auftritt. Dies ist die Standardeinstellung, wenn weder **STGM \_ Direct** noch **STGM \_ transaktiv** angegeben wird.


</dt> </dl> </dd> <dt>

<span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM \_ transaktiv**
</dt> <dd> <dl> <dt>

0x00010000l
</dt> <dt>



Gibt an, dass Änderungen im transaktiven Modus nur gepuffert und geschrieben werden, wenn ein expliziter Commit-Vorgang aufgerufen wird. Um die Änderungen zu ignorieren, müssen Sie die [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) -Methode in der [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)-, [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)-oder [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle aufrufen. Die Implementierung der com-Verbund Datei von **IStorage** unterstützt keine transaktiven Streams. Dies bedeutet, dass Datenströme nur im direkten Modus geöffnet werden können, und Sie können keine Änderungen an diesen Datenströmen zurücksetzen. transaktive Speicher werden jedoch unterstützt. Die Verbund Datei-, eigenständige und NTFS-Dateisystem Implementierungen von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) unterstützen auf ähnliche Weise keine transaktiven, einfachen Eigenschaften Sätze, da diese Eigenschaften Sätze in Datenströmen gespeichert werden. Das transaktionsset von nicht einfachen Eigenschafts Sätzen, das durch Angeben des **\_ nicht einfache-Flags propsetflag** im *grfFlags* -Parameter von [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)erstellt werden kann, wird jedoch unterstützt.


</dt> </dl> </dd> <dt>

<span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM \_ noscratch**
</dt> <dd> <dl> <dt>

0x00100000l
</dt> <dt>



Gibt an, dass im transaktiven Modus normalerweise eine temporäre Scratch-Datei verwendet wird, um Änderungen zu speichern, bis die **Commit** -Methode aufgerufen wird. Wenn Sie **STGM \_ noscratch** angeben, können Sie den nicht verwendeten Teil der ursprünglichen Datei als Arbeitsbereich verwenden, anstatt für diesen Zweck eine neue Datei zu erstellen. Dies wirkt sich nicht auf die Daten in der ursprünglichen Datei aus, und in bestimmten Fällen kann die Leistung verbessert werden. Es ist nicht zulässig, dieses Flag anzugeben, ohne auch **STGM \_ transaktiv** anzugeben, und dieses Flag kann nur in einem geöffneten Stamm verwendet werden. Weitere Informationen zum noscratch-Modus finden Sie im Abschnitt "Hinweise".


</dt> </dl> </dd> <dt>

<span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM- \_ nosnapshot**
</dt> <dd> <dl> <dt>

0x00200000l
</dt> <dt>



Dieses Flag wird verwendet, wenn ein Speicher Objekt mit **STGM \_ transaktiv** und ohne **STGM- \_ Freigabe \_ exklusiv** oder **STGM- \_ Freigabe deny- \_ \_ Schreibvorgang** geöffnet wird. In diesem Fall verhindert die Angabe von **STGM \_ nosnapshot** , dass die vom System bereitgestellte Implementierung eine Momentaufnahme Kopie der Datei erstellt. Stattdessen werden Änderungen an der Datei an das Ende der Datei geschrieben. Nicht verwendeter Speicherplatz wird erst freigegeben, wenn die Konsolidierung während des Commit durchgeführt wird und nur ein aktueller Writer für die Datei vorhanden ist. Wenn die Datei im Modus keine Momentaufnahme geöffnet ist, kann kein anderer Öffnungsvorgang durchgeführt werden, ohne **STGM \_ nosnapshot** anzugeben. Dieses Flag kann nur in einem Stamm Öffnungsvorgang verwendet werden. Weitere Informationen zum nosnapshot-Modus finden Sie im Abschnitt "Hinweise".


</dt> </dl> </dd> <dt>

<span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM \_ Simple**
</dt> <dd> <dl> <dt>

0x08000000l
</dt> <dt>



Bietet eine schnellere Implementierung einer Verbund Datei in einer begrenzten, aber häufig verwendeten Groß-/Kleinschreibung. Weitere Informationen finden Sie im Abschnitt "Hinweise".


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM \_ Direct- \_ Austausch**
</dt> <dd> <dl> <dt>

0x00400000l
</dt> <dt>



Unterstützt den direkten Modus für Datei Vorgänge mit einem einzelnen Writer und mehreren Lesevorgängen. Weitere Informationen finden Sie im Abschnitt "Hinweise".


</dt> </dl> </dd> <dt>

<span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM \_ deleteonrelease**
</dt> <dd> <dl> <dt>

0x04000000l
</dt> <dt>



Gibt an, dass die zugrunde liegende Datei automatisch zerstört werden soll, wenn das Stamm Speicher Objekt freigegeben wird. Diese Funktion ist besonders nützlich für das Erstellen temporärer Dateien. Dieses Flag kann nur verwendet werden, wenn ein Stamm Objekt erstellt wird, z. b. mit [**stgkreatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Dies ist nicht zulässig, wenn ein Stamm Objekt geöffnet wird, z. b. mit [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), oder wenn ein Unterelement erstellt oder geöffnet wird, z. b. mit [**IStorage:: foatestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream). Es ist auch nicht zulässig, dieses Flag und das STGM- \_ Convert-Flag gleichzeitig zu verwenden.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können diese Flags kombinieren, aber Sie können nur ein Flag aus jeder Gruppe verwandter Flags auswählen. In der Regel muss für alle Funktionen und Methoden, die diese Konstanten verwenden, ein Flag aus den einzelnen Zugriffs-und Freigabe Gruppen angegeben werden. Flags aus anderen Gruppen sind optional.

### <a name="transacted-mode"></a>Transaktiver Modus

Wenn das " **STGM \_ Direct**"-Flag angegeben ist, kann nur eine der folgenden Kombinationen von Flags aus den Zugriffs-und Freigabe Gruppen angegeben werden.

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

Beachten Sie, dass der direkte Modus durch das Fehlen von **STGM- \_ Transaktionen** impliziert wird. Das heißt, wenn weder " **STGM \_ Direct** " noch " **STGM \_ transagiert** " angegeben wird, wird **STGM \_ Direct** angenommen.

Wenn das **\_ transaktive STGM** -Flag angegeben wird, werden Objekte im transaktiven Modus erstellt oder geöffnet. In diesem Modus werden Änderungen an einem Objekt erst beibehalten, wenn ein Commit ausgeführt wird. Beispielsweise werden Änderungen an einem transaktiven Speicher Objekt nicht persistent gespeichert, bis die [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) -Methode aufgerufen wird. Änderungen an einem solchen Speicher Objekt gehen verloren, wenn das Speicher Objekt freigegeben wird (endgültige Version), bevor die **Commit** -Methode aufgerufen wird, oder wenn die [**IStorage:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) -Methode aufgerufen wird.

Wenn ein Objekt im transaktiven Modus erstellt oder geöffnet wird, muss die Implementierung sowohl die ursprünglichen Daten als auch die Updates für diese Daten beibehalten, damit Updates bei Bedarf wieder hergestellt werden können. Dies erfolgt in der Regel durch das Schreiben von Änderungen in einen Grundbereich, bis ein Commit ausgeführt wird, oder durch Erstellen einer Kopie, die als Momentaufnahme bezeichnet wird, der zuletzt ausgeführten Daten.

Wenn ein Stamm Speicher Objekt im transaktiven Modus geöffnet wird, können der Speicherort und das Verhalten der Rohdaten und der Momentaufnahme Kopien gesteuert werden, um die Leistung mit den nosnapshot-Flags " **STGM \_ noscratch** " und " **STGM \_ nosnapshot** " zu optimieren. (Ein Stamm Speicher Objekt wird z. b. aus der [**stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) -Funktion abgerufen; ein Speicher Objekt, das von der [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) -Methode abgerufen wurde, ist ein unter Speicher Objekt.) Normalerweise werden die Daten und Momentaufnahmen der Daten in temporären Dateien gespeichert, die vom Speicher getrennt sind.

Die Auswirkung dieser Flags hängt von der Anzahl der Leser und/oder Writer ab, die auf den Stamm Speicher zugreifen.

Im "Single-Writer"-Fall wird ein Speicher Objekt im Transaktionsmodus für den Schreibzugriff geöffnet, und es kann kein anderer Zugriff auf die Datei vorhanden sein. Das heißt, die Datei wird mit **STGM \_ transaktiv** geöffnet, Zugriff auf **STGM- \_ Schreib** -oder **STGM- \_ Lese** Vorgänge und die Freigabe der **STGM- \_ Freigabe \_ exklusiv**. In diesem Fall werden Änderungen am Speicher Objekt in den Scratch-Bereich geschrieben. Wenn für diese Änderungen ein Commit ausgeführt wird, werden Sie in den ursprünglichen Speicher kopiert. Wenn keine Änderungen am Speicher Objekt tatsächlich vorgenommen werden, werden daher keine unnötigen Datenübertragungen übertragen.

Im Fall von "Multiple-Writer" wird ein transaktives Speicher Objekt für den Schreibzugriff geöffnet, aber es wird in derartigen Form verwendet, um andere Writer zuzulassen. Das heißt, dass das Speicher Objekt mit **STGM \_ transaktiv** geöffnet wird, Zugriff auf **STGM- \_ Schreib** Vorgänge oder STGM-Lesevorgänge hat und die Freigabe von STGM-Freigaben **\_ \_ verweigern \_ gelesen** wird. **\_** Wenn stattdessen die Freigabe von **STGM- \_ Freigabe \_ deny \_** nicht angegeben wird, ist der Fall "Multiple-Writer, Multiple-Reader". In diesen Fällen wird während des Öffnungs Vorgangs eine Momentaufnahme der ursprünglichen Daten erstellt. Daher ist auch dann, wenn keine Änderungen am Speicher vorgenommen werden und/oder wenn er nicht gleichzeitig von einem anderen Writer geöffnet wird, die Datenübertragung während des Öffnens erforderlich. Demzufolge kann die beste Leistung bei der Leistung erreicht werden, indem das Speicher Objekt in der **STGM- \_ Freigabe \_ deny- \_ Schreib** -oder **STGM- \_ Freigabe \_ exklusiver** Modus geöffnet wird. Weitere Informationen darüber, wie für Änderungen ein Commit ausgeführt wird, wenn mehrere Writer vorhanden sind, finden Sie unter [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).

Im Fall von "Single-Writer, Multiple-Reader" wird ein transaktives Speicher Objekt für den Schreibzugriff geöffnet, aber für Leser freigegeben. Das heißt, das Speicher Objekt wird vom Writer mit **STGM- \_ Transaktionen**, den Zugriff auf **STGM- \_ Lese** -oder **STGM- \_ Schreib** Vorgänge und die Freigabe von STGM-Freigaben zum **Verweigern von \_ \_ \_ Schreib** Zugriff geöffnet. Der Speicher wird von Lesern mit **gegm- \_ transaktive**, dem Zugriff auf **STGM- \_ Lese** Vorgänge und der Freigabe der **STGM- \_ Freigabe \_ deny \_ None** geöffnet. In diesem Fall verwendet der Writer den Bereich Scratch zum Speichern von Änderungen, für die kein Commit ausgeführt wurde. Wie in den obigen Fällen gibt es bei dem Reader eine Öffnungszeit-Leistungs Einbuße, während eine Momentaufnahme Kopie der Daten erstellt wird.

In der Regel ist der Grundbereich eine temporäre Datei, getrennt von den ursprünglichen Daten. Wenn Änderungen an der ursprünglichen Datei vorgenommen werden, müssen die Daten aus der temporären Datei übertragen werden. Um diese Datenübertragung zu vermeiden, kann das Flag " **STGM \_ noscratch**" angegeben werden. Wenn dieses Flag angegeben wird, werden Teile der Speicher Objektdatei für den Bereich Scratch anstelle einer separaten temporären Datei verwendet. Folglich kann das Ausführen eines Commits für Änderungen schnell erfolgen, da nur wenige Datenübertragungen erforderlich sind. Der Nachteil ist, dass die Speicherdatei größer werden kann, als Sie andernfalls wäre, da Sie für die ursprünglichen Daten und den Grundbereich groß genug vergrößert werden muss. Um die Daten zu konsolidieren und diesen unnötigen Bereich zu entfernen, öffnen Sie den Stamm Speicher im transaktiven Modus erneut, ohne das Flag " **STGM \_ noscratch** " festzulegen. Nennen Sie dann [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) , wobei das **stgc- \_ konsoliderflag** festgelegt ist.

Der momentaufnahmenbereich ist wie der Scratch-Bereich auch eine temporäre Datei. Dies kann auch mit einem STGM-Flag beeinträchtigt werden. Wenn das Flag " **STGM \_ nosnapshot** " angegeben wird, wird keine separate temporäre Momentaufnahme Datei erstellt. Stattdessen werden die ursprünglichen Daten nie geändert, auch wenn mindestens ein Writer pro Objekt vorhanden ist. Wenn für Änderungen ein Commit ausgeführt wird, werden Sie der Datei hinzugefügt, die ursprünglichen Daten bleiben jedoch intakt. Durch diesen Modus wird die Effizienz gesteigert, da die Laufzeit dadurch reduziert wird, dass während des Öffnungs Vorgangs keine Momentaufnahme erstellt werden muss. Wenn Sie diesen Modus verwenden, kann es jedoch zu einer sehr großen Speicherdatei kommen, da die Daten in der Datei nie überschrieben werden können. Dies gilt nicht für die Größe der Dateien, die im nosnapshot-Modus geöffnet werden.

### <a name="direct-single-writer-multiple-reader-mode"></a>Direkter Single-Writer, Multiple-Reader Modus

Wie bereits beschrieben, ist es möglich, einen einzelnen Writer und mehrere Leser eines Speicher Objekts zu haben, wenn dieses Objekt im transaktiven Modus geöffnet wird. Es ist auch möglich, den Single Writer-multireader-Fall im direkten Modus zu erreichen, indem Sie das " **STGM \_ Direct \_ allemr** "-Flag angeben.

In **STGM \_ Direct- \_ taumr** -Modus ist es möglich, dass ein Aufrufer ein Objekt für den Lese-/Schreibzugriff öffnet, während andere Aufrufer gleichzeitig die Datei für den schreibgeschützten Zugriff geöffnet haben. Es ist nicht zulässig, dieses Flag in Kombination mit dem per **STGM \_ transaktiven** Flag zu verwenden. In diesem Modus öffnet der Writer das-Objekt mit den folgenden Flags:

**STGM \_ direkter \_ Austausch** von "STGM", "STGM"- \| **\_** \| **\_ Freigabe " \_ denywrite** "

und jeder Leser öffnet das Objekt mit den folgenden Flags:

**STGM \_ direkter \_ Austausch** von "STGM" \| **\_ Lesen** \| **STGM- \_ Freigabe \_ verweigern \_**

In diesem Modus muss der Writer exklusiven Zugriff auf das Objekt erhalten, um das Speicher Objekt zu ändern. Dies ist möglich, wenn Sie von allen Lesern geschlossen wurden. Der Writer verwendet die [**idirectschreiterlock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) -Schnittstelle, um diesen exklusiven Zugriff zu erhalten.

### <a name="simple-mode"></a>Einfacher Modus

Der einfache Modus (**STGM \_ Simple**) ist für Anwendungen nützlich, die vollständige Speichervorgänge ausführen. Es ist zwar effizient, weist jedoch die folgenden Einschränkungen auf:

-   Für substorages ist keine Unterstützung vorhanden.
-   Das Speicher Objekt und die Streamobjekte, die daraus abgerufen werden, können nicht gemarshallt werden.
-   Jeder Stream weist eine minimale Größe auf. Wenn beim Freigeben des Streams weniger als die minimalen Bytes in einen Stream geschrieben werden, wird der Datenstrom auf die minimale Größe erweitert. Die Mindestgröße für eine bestimmte [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Implementierung beträgt z. b. 4 KB. Es wird ein Stream erstellt und 1 KB darin geschrieben. Bei der endgültigen Version dieses **IStream** wird die Streamgröße automatisch auf 4 KB erweitert. Wenn Sie anschließend den Stream öffnen und die [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) -Methode aufrufen, wird eine Größe von 4 KB angezeigt.
-   Nicht alle Methoden von [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) oder [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) werden von der Implementierung unterstützt. Weitere Informationen finden Sie unter [IStorage-Verbund Datei Implementierung](istorage-compound-file-implementation.md)und [Implementierung der IStream-Verbund Datei](istream-compound-file-implementation.md).

Das Marshalling [ist das](/windows/desktop/Midl/marshaling-ole-data-types) Verpacken, entpacken und Senden von Schnittstellen Methoden Parametern über Thread-oder Prozess Grenzen hinweg innerhalb eines Remote Prozedur Aufrufs (RPC). Weitere Informationen finden Sie unter Marshalling von [Details](../com/marshaling-details.md) und [Schnittstellen](../com/interface-marshaling.md)Marshalling.

Wenn ein Speicher Objekt von einem Create-Vorgang im einfachen Modus abgerufen wird:

-   Streamelemente können erstellt, aber nicht geöffnet werden.
-   Wenn ein Stream-Element durch Aufrufen von [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)erstellt wird, ist es nicht möglich, einen weiteren Stream zu erstellen, bis das Stream-Objekt freigegeben wird.
-   Nachdem alle Streams geschrieben wurden, wird [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) aufgerufen, um die Änderungen zu leeren.

Wenn ein Speicher Objekt von einem Öffnungsvorgang im einfachen Modus abgerufen wird:

-   Es ist möglich, jeweils nur ein streamelement zu öffnen.
-   Es ist nicht möglich, die Größe eines Streams zu ändern, indem Sie die [**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) -Methode aufrufen oder über das Ende des Streams hinaus suchen oder schreiben. Da allerdings alle Streams eine minimale Größe haben, ist es möglich, den Stream bis zu dieser Größe zu verwenden, auch wenn weniger Daten ursprünglich in den Datenstrom geschrieben wurden. Verwenden Sie die [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) -Methode, um die Größe eines Streams zu ermitteln.

Wenn ein Speicher Element von einem Speicher Objekt geändert wird, das sich nicht im einfachen Modus befindet, ist es nicht mehr möglich, dieses Speicher Element im einfachen Modus zu öffnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Objbase. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**Stgkreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**Stgkreatedocfileonilockbytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
</dt> <dt>

[**Stgkreatestorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**Stgopenstorageex**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> <dt>

[**StgOpenStorageOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
</dt> </dl>

 

