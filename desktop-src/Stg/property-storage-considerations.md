---
title: Überlegungen Storage Eigenschaften
description: IPropertyStorage ReadMultiple liest so viele der im rgpspec-Array angegebenen Eigenschaften wie im Eigenschaftensatz.
ms.assetid: 7540966f-a3b2-46c9-9e04-b15133a517eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 128c5da70ae08c62660e0177187036fddee6ff27ed1d9971b6f95dea7052ecdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662160"
---
# <a name="property-storage-considerations"></a>Überlegungen Storage Eigenschaften

[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) liest so viele der im *rgpspec-Array* angegebenen Eigenschaften wie im Eigenschaftensatz. Solange eine der angeforderten Eigenschaften gelesen wird, ist eine Anforderung zum Abrufen einer eigenschaft, die nicht vorhanden ist, kein Fehler. Stattdessen muss dies dazu führen, dass VT EMPTY für diese Eigenschaft bei der Rückgabe in das \_ *rgvar-Array* \[ \] geschrieben wird. Wenn keine der angeforderten Eigenschaften vorhanden ist, sollte die Methode S FALSE zurückgeben \_ und VT \_ EMPTY in jeder [**PROPVARIANT festlegen.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) Wenn ein anderer Fehler zurückgegeben wird, werden keine Eigenschaftswerte abgerufen, und der Aufrufer muss sich keine Gedanken über deren Freigabe machen.

Der *rgpspec-Parameter* ist ein Array von [**PROPSPEC-Strukturen,**](/windows/win32/api/propidlbase/ns-propidlbase-propspec) die für jede Eigenschaft entweder ihren Eigenschaftenbezeichner oder, wenn eine zugewiesen ist, einen Zeichenfolgenbezeichner angeben. Sie können eine Zeichenfolge einem Eigenschaftenbezeichner zuordnen, indem Sie [**IPropertyStorage::WritePropertyNames aufrufen.**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames) Die Verwendung von Eigenschaftenbezeichnern ist jedoch wahrscheinlich deutlich effizienter als die Verwendung von Zeichenfolgen.

Eigenschaften, die vom Zeichenfolgennamen (PRSPEC LPWSTR) angefordert werden, werden \_ Eigenschaftsbezeichnern (IDs) ohne Unterscheidung nach Groß-/Kleinschreibung zugeordnet, wie sie im aktuellen Eigenschaftensatz (und gemäß dem aktuellen System-Locale) angegeben werden.

When the property type is VT\_LPSTR and the property is read from an ANSI property set, that is, the code page for the property set is set to something other than Unicode, the value of the property uses the same code page as the property set. When a VT\_LPSTR property is read from a Unicode property set, the value of the property uses the system's current default ANSI code page, that is, the code page returned from the **GetACP** function.

Eine [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)wird mit Ausnahme derer, die Zeiger auf Streams und Speicher sind, als einfache **PROPVARIANT bezeichnet.** Diese einfachen **PROPVARIANT-S** empfangen Daten nach Wert, sodass ein Aufruf von [**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) eine Kopie der Daten liefert, die der Aufrufer dann besitzt. Rufen Sie zum Erstellen oder Aktualisieren dieser Eigenschaften [**IPropertyStorage::WriteMultiple auf.**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)

Im Gegensatz dazu sind die Variantentypen VT \_ STREAM, VT \_ STREAMED \_ OBJECT, VT STORAGE und \_ VT STORED \_ OBJECT nicht einfache \_ Eigenschaften, da die Methode anstelle eines Werts einen Zeiger auf die angegebene Schnittstelle abruft, aus der die Daten dann gelesen werden können. Diese Typen ermöglichen das Speichern großer Mengen von Informationen über eine einzelne Eigenschaft. Es gibt mehrere Probleme, die bei der Verwendung von nicht einfachen Eigenschaften auftreten.

Um diese Eigenschaften wie für die anderen Eigenschaften zu erstellen, rufen Sie [**IPropertyStorage::WriteMultiple auf.**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) Anstatt die gleiche Methode zum Aktualisieren auf aufruft, ist es jedoch effizienter, zuerst [**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) auf aufruft, um den Schnittstellenzeiger auf den Stream oder Speicher zu erhalten, und dann Daten mithilfe der [**IStream-**](/windows/desktop/api/Objidl/nn-objidl-istream) oder [**IStorage-Methoden**](/windows/desktop/api/Objidl/nn-objidl-istorage) zu schreiben. Ein Stream oder Speicher, der über eine Eigenschaft geöffnet wird, wird immer im direkten Modus geöffnet, sodass keine zusätzliche Ebene geschachtelter Transaktionen eingeführt wird. Je nachdem, wie sie über [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)geöffnet oder erstellt wurde, kann es jedoch trotzdem eine Transaktion für die Eigenschaft geben, die als Ganzes festgelegt wurde. Darüber hinaus werden die Beim Öffnen oder Erstellen des Eigenschaftensets angegebenen Zugriffs- und Freigabemodustags an eigenschaftsbasierte Streams oder Speicher übergeben.

Die Lebensdauer von eigenschaftsbasierten Stream- oder Speicherzeigern, obwohl sie theoretisch unabhängig von ihren zugeordneten [**IPropertyStorage-**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) und [**IPropertySetStorage-Zeigern**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) sind, sind tatsächlich davon abhängig. Die über den Stream oder Speicher sichtbaren Daten sind mit der Transaktion des Eigenschaftenspeicherobjekts verknüpft, aus dem sie abgerufen werden, genau wie bei einem Speicherobjekt (das [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)unterstützt) mit enthaltenen Stream- und Speicherunterobjekten. Wenn die Transaktion für das übergeordnete Objekt abgebrochen wird, kann nicht mehr auf vorhandene [**IStream-**](/windows/desktop/api/Objidl/nn-objidl-istream) und **IStorage-Zeiger** zugegriffen werden, die diesem Objekt untergeordnet sind. Da **IPropertyStorage** die einzige Schnittstelle im Eigenschaftsspeicherobjekt ist, wird die nützliche Lebensdauer der enthaltenen **IStream-** und **IStorage-Zeiger** durch die Lebensdauer der **IPropertyStorage-Schnittstelle** gebunden.

Die Implementierung muss auch mit der Situation umgehen, in der dieselbe Stream- oder Speicherwerteigenschaft mehrmals über dieselbe [**IPropertyStorage-Schnittstelleninstanz**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) angefordert wird. In der COM-Verbunddateiimplementierung ist das Öffnen z. B. erfolgreich oder nicht erfolgreich, je nachdem, ob die Eigenschaft bereits geöffnet ist oder nicht.

Ein weiteres Problem ist, dass mehrere Geöffnete im Transaktionsmodus geöffnet werden. Das Ergebnis hängt von der Isolationsstufe ab, die durch einen Aufruf von [**IPropertySetStorage-Methoden**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) angegeben wurde (entweder die [**Open-**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) oder [**Create-Methode**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) über die STGM-Flags), als der Eigenschaftenspeicher geöffnet wurde.

Wenn der Aufruf zum Öffnen des Eigenschaftensets Lese-/Schreibzugriff angibt, werden [**IStorage-**](/windows/desktop/api/Objidl/nn-objidl-istorage) und [**IStream-Werteigenschaften**](/windows/desktop/api/Objidl/nn-objidl-istream)immer mit Lese-/Schreibzugriff geöffnet. Daten können dann über diese Schnittstellen geschrieben werden, wodurch der Wert der -Eigenschaft geändert wird. Dies ist die effizienteste Methode zum Aktualisieren dieser Eigenschaften. Der -Eigenschaftswert selbst verfügt nicht über eine zusätzliche Ebene der Transaktionsschachtelung, sodass Änderungen unter der Transaktion (falls dies der Fall ist) für das Eigenschaftenspeicherobjekt gelten.

## <a name="storage-and-stream-properties"></a>Storage und Streameigenschaften

Um einen Stream oder ein Speicherobjekt in einen Eigenschaftensatz zu schreiben, muss der Eigenschaftensatz als nicht einfach erstellt worden sein. Weitere Informationen zu einfachen und nicht einfachen Eigenschaftensätzen finden Sie im Abschnitt Storage stream objects for a Property Set (Streamobjekte [für einen Eigenschaftensatz).](storage-vs--stream-for-a-property-set.md) Die folgenden Eigenschaftentypen, wie im *vt-Feld* der *rgvar-Arrayelemente* angegeben, sind Stream- oder Speichertypen: VT \_ STREAM, VT \_ STORAGE, VT \_ STREAMED \_ OBJECT, VT \_ STORED \_ OBJECT.

Um einen Stream oder ein Speicherobjekt als Eigenschaft in einen nicht einfachen Eigenschaftensatz zu schreiben, rufen Sie [**IPropertyStorage::WriteMultiple auf.**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) Sie würden diese Methode auch aufrufen, um einfache Eigenschaften zu aktualisieren, aber es ist keine effiziente Möglichkeit, Stream- und Speicherobjekte in einem Eigenschaftensatz zu aktualisieren. Dies liegt daran, dass beim Aktualisieren einer dieser Eigenschaften durch einen Aufruf von **WriteMultiple** im Eigenschaftenspeicherobjekt eine Kopie der übergebenen Daten erstellt wird und die [**IStorage-**](/windows/desktop/api/Objidl/nn-objidl-istorage) oder [**IStream-Zeiger**](/windows/desktop/api/Objidl/nn-objidl-istream) nicht über die Dauer dieses Aufrufs hinaus beibehalten werden. In der Regel ist es effizienter, Stream- oder Speicherobjekte direkt zu aktualisieren, indem Sie zuerst [**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) aufrufen, um den Schnittstellenzeiger auf den Stream oder Speicher zu erhalten, und dann Daten über die **IStream-** oder **IStorage-Methoden** schreiben.

Beispielsweise können Sie [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) aufrufen, um einen NULL-Stream oder ein **Speicherobjekt** zu schreiben. Die Implementierung erstellt dann ein leeres Objekt im Eigenschaftensatz. Sie können dann zugriff auf dieses Objekt erhalten, indem Sie [**IPropertyStorage::ReadMultiple aufrufen.**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) Wenn Sie die Aktualisierung dieses Objekts abgeschlossen haben, müssen Sie es nicht in den Eigenschaftensatz schreiben, da Ihre Updates direkt in den Eigenschaftensatz gehen.

Ein Stream oder Speicher, der über eine Eigenschaft geöffnet wird, wird immer im direkten Modus geöffnet, sodass keine zusätzliche Ebene geschachtelter Transaktionen eingeführt wird. Es kann weiterhin eine Transaktion für die Eigenschaft geben, die als Ganzes festgelegt ist. (Beispiel: [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) wurde durch Aufrufen von [**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) mit dem STGM erhalten. \_ TransactED-Flag im *grfmode-Parameter* festgelegt.) Darüber hinaus wird ein eigenschaftsbasierter Stream oder Speicher nach Möglichkeit im Lese-/Schreibmodus geöffnet, wenn der Modus für den Eigenschaftensatz verwendet wird. Andernfalls wird der Lesemodus verwendet.

Wie bereits erwähnt, wird beim Schreiben eines Streams oder Speicherobjekts in einen Eigenschaftensatz mit der [**WriteMultiple-Methode**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) eine Kopie des Objekts erstellt. Wenn eine solche Kopie für ein Streamobjekt erstellt wird, beginnt der Kopiervorgang an der aktuellen Suchposition der Quelle. Die Suchposition ist bei einem Fehler nicht definiert, aber bei Erfolg befindet sie sich am Ende des Streams. Der Suchzeiger wird nicht an seiner ursprünglichen Position wiederhergestellt.

Wenn ein Stream oder eine Speichereigenschaft aus einem Eigenschaftensatz mit [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)gelesen wurde, wird weiterhin geöffnet gehalten, und ein nachfolgender Aufruf von [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) für dieselbe Eigenschaft wird durchgeführt, der **WriteMultiple-Vorgang** ist erfolgreich. Der zuvor geöffnete Stream oder die zuvor geöffnete Speichereigenschaft wird in den zustandsbewollten Zustand gesetzt (alle Aufrufe an ihn geben den STG \_ E \_ REVERTED-Fehler zurück).

Wenn die [**WriteMultiple-Methode**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) beim Schreiben eines Arrays von Eigenschaften oder sogar einzelne nicht einfache Eigenschaften einen Fehler zurückgibt, ist die tatsächlich geschriebene Datenmenge nicht definiert.

## <a name="reference-properties"></a>Verweiseigenschaften

Wenn eine angegebene [**PROPVARIANT-Struktur**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) das VT BYREF-Flag in seinem vt-Member enthält, ist die zugeordnete Eigenschaft \_ eine Verweiseigenschaft.  Eine Verweiseigenschaft wird automatisch dereferenziert, bevor der Wert in den Eigenschaftensatz geschrieben wird. Wenn beispielsweise der **vt-Member** der **PROPVARIANT-Struktur** einen Wert vom Typ VT BYREF VT I4 angibt, ist der geschriebene tatsächliche Wert ein \_ \| \_ VT \_ I4-Typ. Ein nachfolgender Aufruf der [**IPropertyStorage::ReadMultiple-Methode**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) gibt einen Wert als VT \_ I4 zurück. Die Verwendung von Verweiseigenschaften ähnelt dem Aufrufen der [VariantCopyInd-Funktion.](/windows/win32/api/oleauto/nf-oleauto-variantcopyind) [VariantCopyInd gibt](/windows/win32/api/oleauto/nf-oleauto-variantcopyind) die Zielvariante frei und macht eine Kopie der VariantARG-Quelldatei. Dabei wird die erforderliche Dereferenzierung durchgeführt, wenn als Quelle VT \_ BYREF angegeben ist. Diese Funktion ist nützlich, wenn eine Kopie einer Variante benötigt wird, und um zu gewährleisten, dass es sich nicht um VT BYREF handelt, z. B. bei der Behandlung von Argumenten in einer Implementierung von \_ [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke).

## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Es wird empfohlen, Eigenschaftensätze als Unicode zu erstellen, indem sie das PROPSETFLAG ANSI-Flag nicht im \_ *grfFlags-Parameter* von [**IPropertySetStorage::Create festlegen.**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) Es wird auch empfohlen, die Verwendung von VT LPSTR-Werten zu vermeiden und stattdessen \_ VT \_ LPWSTR-Werte zu verwenden. Wenn die Codepage für den Eigenschaftensatz Unicode ist, werden VT LPSTR-Zeichenfolgenwerte beim Speichern in Unicode und beim Abrufen wieder in \_ Multibyte-Zeichenfolgenwerte konvertiert. Wenn die Codepage des Eigenschaftensets nicht Unicode ist, werden Eigenschaftsnamen, VT BSTR-Zeichenfolgen und nicht einfache Eigenschaftswerte beim Speichern in Multibytezeichenfolgen konvertiert und beim Abrufen wieder in Unicode konvertiert, und alle verwenden die aktuelle \_ System-ANSI-Codepage.

## <a name="notes-to-implementers"></a>Hinweise für Ausführende

Bei der Zuweisung eines Eigenschaftenbezeichners kann die Implementierung jeden Wert auswählen, der derzeit nicht im Eigenschaftensatz für einen Eigenschaftenbezeichner verwendet wird, solange er nicht 0 oder 1 oder größer als 0x80000000 ist, die alle reservierte Werte sind. Der *propidNameFirst-Parameter* legt einen Mindestwert für Eigenschaftsbezeichner innerhalb des Sets fest und muss größer als 1 und kleiner als 0x80000000. Siehe Abschnitt "Hinweise" weiter oben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPropertyStorage-Verbunddateiimplementierung](ipropertystorage-compound-file-implementation.md)
</dt> <dt>

[IPropertyStorage-NTFS-Dateisystemimplementierung](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[Eigenständige IPropertyStorage-Implementierung](ipropertystorage-stand-alone-implementation.md)
</dt> </dl>

 

 