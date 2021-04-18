---
description: Die cbasezucator-Klasse ist eine abstrakte Basisklasse, die einen Zuweiser implementiert. Zuweisungen machen die imemzuzucator-Schnittstelle verfügbar.
ms.assetid: 3c9003d8-f15c-4e85-9712-9aaa87dffdf3
title: Cbasezucator-Klasse (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 068dd45ee3ffac5c3b915c3b0cdd8bc87756377e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357658"
---
# <a name="cbaseallocator-class"></a>Cbasezucator-Klasse

![cbasezucator-Klassenhierarchie](images/filter10.png)

Die **cbasezucator** -Klasse ist eine abstrakte Basisklasse, die einen Zuweiser implementiert. Zuweisungen machen die [**imemzuzucator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle verfügbar.

Eine *Zuweisung* ist ein Objekt, das Speicherpuffer zuordnet. Die Zuweisung verwaltet eine Liste der verfügbaren Puffer. Wenn ein Client (im Allgemeinen ein Filter) einen Puffer anfordert, ruft die Zuweisung einen Puffer aus der Liste ab. Der Client füllt den Puffer mit Daten und übergibt den Puffer möglicherweise an ein anderes Objekt. Schließlich wird der Puffer freigegeben, und die Zuweisung gibt ihn an die Liste der verfügbaren Puffer zurück.

Jeder Puffer wird von einem Objekt gekapselt, das als *Medien Beispiel* bezeichnet wird. Mit Medien Beispielen können Sie Zeiger auf Speicherblöcke innerhalb des Component Object Model (com)-Frameworks verpacken. In den Medien Beispielen wird die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle verfügbar gemacht und mithilfe der [**cmediasample**](cmediasample.md) -Klasse implementiert. Ein Medien Beispiel enthält einen Zeiger auf den zugeordneten Puffer, auf den durch Aufrufen der [**imediasample:: getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) -Methode zugegriffen werden kann. Weitere Informationen finden Sie unter [Beispiele und Zuweisungen](samples-and-allocators.md).

Um diese Klasse zu verwenden, führen Sie die folgenden Schritte aus:

1.  Aufrufen der [**cbasezucator:: SetProperties**](cbaseallocator-setproperties.md) -Methode, um die Puffer Anforderungen anzugeben, einschließlich der Anzahl der Puffer und der Größe der einzelnen Puffer.
2.  Nennen Sie die [**cbaseallocator:: Commit**](cbaseallocator-commit.md) -Methode, um die Puffer zuzuordnen.
3.  Rufen Sie die [**cbasezucator:: GetBuffer**](cbaseallocator-getbuffer.md) -Methode auf, um Medien Beispiele abzurufen. Diese Methode wird blockiert, bis das nächste Beispiel verfügbar wird.
4.  Wenn Sie mit den einzelnen Beispielen abgeschlossen sind, können Sie die **IUnknown:: Release** -Methode für das Beispiel aufzurufen. Das Beispiel wird nicht gelöscht, wenn der Verweis Zähler Null erreicht. Stattdessen wird das Beispiel in die kostenlose Liste des zuordcators zurückgegeben.
5.  Wenn Sie die Zuweisung durchgeführt haben, können Sie die [**cbasebelegcator::D ecommit**](cbaseallocator-decommit.md) -Methode verwenden, um den Speicher für die Puffer freizugeben.

Die [**Commit**](cbaseallocator-commit.md) -Methode ruft die virtuelle Methode [**cbasebelegcator:: belegc**](cbaseallocator-alloc.md)auf, die den Speicher für die Puffer zuordnet. Die [**Decommit**](cbaseallocator-decommit.md) -Methode ruft die reine virtuelle Methode [**cbasebelegcator:: Free**](cbaseallocator-free.md)auf, die den Arbeitsspeicher freigibt. Abgeleitete Klassen müssen diese beiden Methoden überschreiben.

Die [**cmemzuordcator**](cmemallocator.md) -Basisklasse wird von **cbasezukator** abgeleitet. Die Filter Basisklassen verwenden die **cmemzuordcator** -Klasse.



| Geschützte Member-Variablen                                                   | BESCHREIBUNG                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**m \_ lfree**](cbaseallocator-m-lfree.md)                                   | Zeiger auf eine Liste der verfügbaren (freien) Medien Beispiele.                                       |
| [**m \_ hsem**](cbaseallocator-m-hsem.md)                                     | Semaphore, die signalisiert wird, wenn ein Beispiel verfügbar wird.                                |
| [**m \_ lwarteschlange**](cbaseallocator-m-lwaiting.md)                             | Anzahl der Threads, die auf Stichproben warten.                                                      |
| [**m \_ lCount**](cbaseallocator-m-lcount.md)                                 | Anzahl der Puffer, die bereitgestellt werden sollen.                                                              |
| [**m \_ lzugewiesen**](cbaseallocator-m-lallocated.md)                         | Anzahl der aktuell zugeordneten Puffer.                                                     |
| [**m \_ LSIZE**](cbaseallocator-m-lsize.md)                                   | Die Größe der einzelnen Puffer.                                                                       |
| [**m \_ lausrichtung**](cbaseallocator-m-lalignment.md)                         | Die Ausrichtung der einzelnen Puffer.                                                                  |
| [**m \_ lprefix**](cbaseallocator-m-lprefix.md)                               | Präfix der einzelnen Puffer.                                                                     |
| [**m \_ bchanged**](cbaseallocator-m-bchanged.md)                             | Flag zum angeben, ob sich die Puffer Anforderungen geändert haben.                              |
| [**Mio. \_ bcommit**](cbaseallocator-m-bcommitted.md)                         | Flag zum angeben, ob für die Zuweisung ein Commit ausgeführt wurde.                                  |
| [**m \_ bdecommitinprogress**](cbaseallocator-m-bdecommitinprogress.md)       | Flag zum angeben, ob ein Decommit-Vorgang ausgeführt wird.                               |
| [**m \_ pnotify**](cbaseallocator-m-pnotify.md)                               | Zeiger auf eine Rückruf Schnittstelle, die aufgerufen wird, wenn Beispiele freigegeben werden.                |
| [**m \_ fenablereleasecallback**](cbaseallocator-m-fenablereleasecallback.md) | Flag zum angeben, ob der releaserückruf aktiviert ist.                                   |
| Geschützte Methoden                                                            | BESCHREIBUNG                                                                                |
| [**Zuordnungseinheits**](cbaseallocator-alloc.md)                                        | Belegt Speicher für die Puffer. Virtu.                                                 |
| Öffentliche Methoden                                                               | BESCHREIBUNG                                                                                |
| [**Cbasezucator**](cbaseallocator-cbaseallocator.md)                      | Konstruktormethode.                                                                        |
| [**~ Cbasezucator**](cbaseallocator--cbaseallocator.md)                   | Dekonstruktormethode.                                                                         |
| [**Setnotify**](cbaseallocator-setnotify.md)                                | Veraltet.                                                                                  |
| [**Getfrecount**](cbaseallocator-getfreecount.md)                          | Ruft die Anzahl von Medien Beispielen ab, die nicht verwendet werden.                                 |
| [**Notifysample**](cbaseallocator-notifysample.md)                          | Gibt alle Threads frei, die auf Beispiele warten.                                         |
| [**Setwaiting**](cbaseallocator-setwaiting.md)                              | Erhöht die Anzahl der wartenden Threads.                                                   |
| Reine virtuelle Methoden                                                         | BESCHREIBUNG                                                                                |
| [**Kostenlos**](cbaseallocator-free.md)                                          | Gibt den gesamten Puffer Arbeitsspeicher frei.                                                         |
| Imemzuordcator-Methoden                                                        | BESCHREIBUNG                                                                                |
| [**SetProperties**](cbaseallocator-setproperties.md)                        | Gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an.                   |
| [**GetProperties**](cbaseallocator-getproperties.md)                        | Ruft die Anzahl der Puffer ab, die von der Zuweisung erstellt werden, sowie die Puffer Eigenschaften. |
| [**Einzusetzen**](cbaseallocator-commit.md)                                      | Weist den Speicher für die Puffer zu.                                                      |
| [**Decommit**](cbaseallocator-decommit.md)                                  | Führt einen Commit für die Puffer aus.                                                                     |
| [**GetBuffer**](cbaseallocator-getbuffer.md)                                | Ruft ein Medien Beispiel ab, das einen Puffer enthält.                                           |
| [**ReleaseBuffer**](cbaseallocator-releasebuffer.md)                        | Gibt ein Medien Beispiel zur Liste der Beispiele für freie Medien zurück.                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Bereitstellen einer benutzerdefinierten Zuweisung](providing-a-custom-allocator.md)
</dt> </dl>

 

 




