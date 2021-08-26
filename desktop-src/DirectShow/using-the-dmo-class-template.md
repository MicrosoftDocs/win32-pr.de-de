---
description: Verwenden der DMO-Klassenvorlage
ms.assetid: 5193ad08-aaee-47e3-93eb-a126a66d8f23
title: Verwenden der DMO-Klassenvorlage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 205ee51953aff35ef5b05790b45fcd0bdf3bcd753239a521e40ca796c21b0a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130900"
---
# <a name="using-the-dmo-class-template"></a>Verwenden der DMO-Klassenvorlage

DirectShow enthält eine Klassenvorlage, [**IMediaObjectImpl,**](imediaobjectimpl-class-template.md)zum Implementieren von DMOs. Die Vorlage verarbeitet viele der "Buchhaltungsaufgaben", z. B. das Überprüfen von Eingabeparametern. Mithilfe der Vorlage können Sie sich auf die Funktionen konzentrieren, die für Ihre DMO spezifisch sind. Darüber hinaus trägt die Vorlage dazu bei, sicherzustellen, dass Sie eine stabile Implementierung erstellen. Die Vorlage wird in der Headerdatei Dmoimpl.h definiert, die sich im Verzeichnis Include des SDK befindet.

Die **IMediaObjectImpl-Vorlage** erbt die [**IMediaObject-Schnittstelle.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) Um eine DMO mithilfe der Vorlage zu erstellen, definieren Sie eine neue Klasse, die von **IMediaObjectImpl** abgeleitet wird. Die Vorlage implementiert alle **IMediaObject-Methoden.** In den meisten Fällen ruft die Vorlage eine entsprechende private Methode für die abgeleitete Klasse auf. Die Vorlage bietet die folgenden Features:

-   Grundlegende Parameterüberprüfung. Die Vorlagenmethoden überprüfen, ob die erforderlichen Parameter nicht **NULL** sind, dass stream-Indizes innerhalb des Bereichs liegen und dass Flags gültig sind.
-   Sperren. Die Vorlagenmethoden rufen die beiden internen Methoden **Lock** und **Unlock** auf, um Vorgänge auf dem DMO zu serialisieren. Dieses Feature stellt sicher, dass die DMO threadsicher ist.
-   Medientypen. Die Vorlage speichert die vom Client festgelegten Medientypen und stellt Zugriffsmethoden für die Medientypen bereit.
-   Streaming. Die Vorlage verhindert das Streaming, bis der Client Medientypen für alle nicht optionalen Streams festgelegt hat. Außerdem wird sichergestellt, dass die [**IMediaObject::AllocateStreamingResources-Methode**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) aufgerufen wird, bevor das Streaming beginnt, wodurch sichergestellt wird, dass Ressourcen zugeordnet werden.

Die abgeleitete Klasse muss die **IUnknown-Schnittstelle** implementieren. Die Vorlage stellt diese Schnittstelle nicht bereit. Sie können die Active Template Library (ATL) verwenden, um **IUnknown** zu implementieren, oder Sie können eine andere Implementierung bereitstellen. Die Vorlage implementiert auch nicht den Sperrmechanismus. Die abgeleitete Klasse muss die **Lock-** und **Unlock-Methoden** implementieren. Wenn Sie Ihre Klasse mit ATL erstellen, können Sie die ATL-Standardimplementierungen verwenden.

**Deklarieren der abgeleiteten Klasse**

Die **IMediaObjectImpl-Klassenvorlage** wird wie folgt deklariert:


```C++
template <class _DERIVED_, int NUMBEROFINPUTS, int NUMBEROFOUTPUTS>
class IMediaObjectImpl : public ImediaObject
```



Die drei Vorlagenparameter sind \_ \_ DERIVED, NUMBEROFINPUTS und NUMBEROFOUTPUTS. Legen Sie \_ DERIVED auf den Namen Ihrer Klasse \_ fest. Die beiden anderen Parameter definieren die Anzahl der Eingabe- und Ausgabestreams auf dem DMO. Verwenden Sie beispielsweise die folgende Deklaration, um eine DMO Klasse namens CMyDmo zu erstellen, die einen Eingabestream und zwei Ausgabestreams unterstützt:


```C++
class CMyDmo : public IMediaObjectImpl<CMyDmo, 1, 2>
```



Im weiteren Verlauf dieses Abschnitts wird beschrieben, wie die Vorlage die verschiedenen Methoden in **IMediaObject** implementiert.

**Methoden zum Festlegen von Medientypen**

Mit den folgenden Methoden werden Medientypen auf dem DMO festgelegt oder abgerufen:

-   **GetInputType**, **GetOutputType**. Diese Methoden geben bevorzugte Medientypen nach Streamnummer und Typindex zurück. Die Vorlage ruft **InternalGetInputType** oder **InternalGetOutputType** für die abgeleitete Klasse auf.
-   **SetInputType**, **SetOutputType**. Diese Methoden legen den Medientyp für einen Stream fest, testen einen Medientyp oder löschen einen Medientyp. Um den Medientyp zu überprüfen, ruft die Vorlage **InternalCheckInputType** oder **InternalCheckOutputType** für die abgeleitete Klasse auf. Die abgeleitete Klasse gibt S \_ OK zurück, um den Typ zu akzeptieren, oder DMO \_ E \_ INVALIDTYPE, um den Typ abzulehnen. Die Vorlage verarbeitet das Festlegen oder Löschen des Medientyps.
-   **GetInputCurrentType**, **GetOutputCurrentType**. Diese Methoden geben den aktuellen Medientyp für einen Stream oder DMO \_ E TYPE NOT SET \_ \_ \_ zurück, wenn kein Typ festgelegt ist. Die Vorlage implementiert diese Methoden vollständig.

**Informationsmethoden**

Die folgenden Methoden stellen Informationen zum DMO bereit.

-   **GetInputMaxLatency**, **SetInputMaxLatency**. Diese Methoden rufen die maximale Latenz ab oder legen sie fest. Die Vorlage ruft **InternalGetInputMaxLatency** oder **InternalSetInputMaxLatency** für die abgeleitete Klasse auf.
-   **GetInputSizeInfo**, **GetOutputSizeInfo**. Diese Methoden geben die Pufferanforderungen der DMO für einen angegebenen Stream zurück. Wenn für diesen Stream kein Medientyp festgelegt wurde, gibt die Vorlage DMO \_ E TYPE NOT SET \_ \_ \_ zurück. Andernfalls ruft sie **InternalGetInputSizeInfo** oder **InternalGetOutputSizeInfo** für die abgeleitete Klasse auf.
-   **GetInputStreamInfo**, **GetOutputStreamInfo**. Diese Methoden geben verschiedene Flags zurück, die angeben, wie der Client die Daten formatieren soll. Die Vorlage ruft **InternalGetInputStreamInfo** oder **InternalGetOutputStreamInfo** für die abgeleitete Klasse auf.
-   **GetStreamCount**. Diese Methode gibt die Anzahl der Eingabe- und Ausgabestreams zurück. Die Vorlage implementiert diese Methode mithilfe der Vorlagenparameter.

**Methoden für die Ressourcenzuordnung**

-   Die **AllocateStreamingResources-Methode** ordnet alle Ressourcen zu, die der DMO benötigt, bevor das Streaming beginnt. Die **FreeStreamingResources-Methode** gibt die gleichen Ressourcen frei. Die Vorlage ruft **InternalAllocateStreamingResources** bzw. **InternalFreeStreamingResources** auf.

Der Client der DMO ist nicht erforderlich, um diese Methoden aufzurufen, aber die Vorlage ruft **allocateStreamingResources** automatisch auf, bevor das Streaming gestartet wird. Daher kann die DMO davon ausgehen, dass Ressourcen zum Zeitpunkt des Aufrufs von **ProcessInput** ordnungsgemäß zugeordnet wurden. Der DMO sollte **FreeStreamingResources** in seinem Destruktor aufrufen.

Wenn die Vorlage **InternalAllocateStreamingResources aufruft,** wird außerdem ein internes Flag festgelegt, sodass diese Methode erst wieder aufgerufen wird, wenn **InternalFreeStreamingResources** aufgerufen wird. Dadurch wird sichergestellt, dass Ressourcen nicht versehentlich neu zugeordnet werden, was zu Speicherverlusten führen kann.

**Methoden für das Streaming**

Die folgenden Methoden werden zum Streamen von Daten verwendet:

-   **GetInputStatus**. Diese Methode gibt an, ob die DMO derzeit Eingaben akzeptieren kann. Die Vorlage ruft **InternalAcceptingInput** für die abgeleitete Klasse auf. Wenn die DMO Eingaben akzeptieren kann, gibt die abgeleitete Klasse S \_ OK zurück, und die Vorlage legt das DMO \_ INPUT \_ STATUSF ACCEPT \_ \_ DATA-Bit im *dwFlags-Parameter* fest. Andernfalls gibt die abgeleitete Klasse S FALSE zurück, \_ und die Vorlage legt *dwFlags* auf 0 (null) fest.
-   **ProcessInput**. Diese Methode verarbeitet einen Eingabepuffer. Die Vorlage ruft **AllocateStreamingResources auf,** wie zuvor beschrieben. Anschließend ruft sie **InternalAcceptingInput** für die abgeleitete Klasse auf. Wenn die DMO neue Eingaben akzeptieren kann, ruft die Vorlage **InternalProcessInput auf.**
-   **ProcessOutput**. Diese Methode verarbeitet einen Satz von Ausgabepuffern, einen Puffer für jeden Ausgabestream. Die Vorlage ruft **AllocateStreamingResources** und dann **InternalProcessOutput** auf.
-   **Diskontinuität**. Diese Methode signalisiert eine Diskontinuität in einem Eingabestream. Die Vorlage ruft **InternalAcceptingInput** für die abgeleitete Klasse auf. Wenn diese Methode S \_ OK zurückgibt, ruft die Vorlage **InternalDiscontinuity** für die abgeleitete Klasse auf.
-   **Leeren Sie**. Diese Methode leert die DMO. Die Vorlage ruft **InternalFlush** für die abgeleitete Klasse auf. Der DMO sollte alle Eingabepuffer verwerfen, die noch verarbeitet werden müssen.

Die Vorlage bietet keine direkte Unterstützung für die [**IMediaObjectInPlace-Schnittstelle.**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace)

**Methoden für sperren**

Sperren werden verwendet, um den Zustand der DMO in einer Multithreadumgebung zu schützen. In einem ATL-Projekt verursacht die [**IMediaObject::Lock-Methode**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-lock) einen Namenskonflikt mit der ATL **Lock-Methode.** Um den Konflikt zu lösen, benennt die Vorlage die **IMediaObject-Methode** in **DMOLock** um. Definieren Sie beim Kompilieren der abgeleiteten Klasse FIX \_ LOCK \_ NAME, bevor Sie die Headerdatei Dmo.h hinzufügen:


```C++
#define FIX_LOCK_NAME
#include <dmo.h>
```



Diese Direktive bewirkt, dass der Präprozessor **DMOLock** in der Deklaration der **IMediaObject-Schnittstelle** durch **Lock** ersetzt. Anwendungen können die Methode weiterhin mit dem Namen **Lock** aufrufen, da sich die vtable-Reihenfolge nicht ändert. Die **DMOLock-Methode** ruft **Lock oder** Unlock für **die** abgeleitete Klasse auf. Wenn Sie ATL zum Implementieren der abgeleiteten Klasse verwenden, sind diese Methoden bereits von ATL definiert, sodass kein zusätzlicher Code erforderlich ist. Wenn Sie ATL nicht verwenden, müssen Sie die **Lock-** und **Unlock-Methoden** in der abgeleiteten Klasse bereitstellen.

Die Vorlage sperrt die DMO in jeder der **IMediaObject-Methoden** automatisch. Die abgeleitete Klasse muss möglicherweise DMO öffentlichen Methoden sperren, die sie implementiert (z. B. wenn **sie IMediaObjectInPlace unterstützt).** Die Klassenvorlage stellt auch die interne Hilfsklasse [**IMediaObjectImpl::LockIt**](imediaobjectimpl-lockit.md)zur Auswahl, die zum Sperren und Entsperren der DMO.

**Zusammenfassung**

Für die folgenden **IMediaObject-Methoden** ruft die Vorlage eine entsprechende Methode mit der gleichen Signatur für die abgeleitete Klasse auf. Die abgeleitete Klasse muss jede der in der zweiten Spalte gezeigten Methoden implementieren.



| IMediaObject-Methode            | Abgeleitete Klassenmethode                   |
|--------------------------------|----------------------------------------|
| **AllocateStreamingResources** | **InternalAllocateStreamingResources** |
| **Diskontinuität**              | **InternalDiscontinuity**              |
| **Leerung**                      | **InternalFlush**                      |
| **FreeStreamingResources**     | **InternalFreeStreamingResources**     |
| **GetInputMaxLatency**         | **InternalGetInputMaxLatency**         |
| **GetInputSizeInfo**           | **InternalGetInputSizeInfo**           |
| **GetInputStreamInfo**         | **InternalGetInputStreamInfo**         |
| **GetInputType**               | **InternalGetInputType**               |
| **GetOutputSizeInfo**          | **InternalGetOutputSizeInfo**          |
| **GetOutputStreamInfo**        | **InternalGetOutputStreamInfo**        |
| **GetOutputType**              | **InternalGetOutputType**              |
| **ProcessInput**               | **InternalProcessInput**               |
| **ProcessOutput**              | **InternalProcessOutput**              |
| **SetInputMaxLatency**         | **InternalSetInputMaxLatency**         |



 

Für die **verbleibenden IMediaObject-Methoden** gibt es keine 1:1-Entsprechung zwischen Vorlagenmethoden und abgeleiteten Klassenmethoden. In der folgenden Tabelle wird zusammengefasst, welche Methoden vollständig von der Vorlage implementiert werden und welche Methoden andere Methoden für die abgeleitete Klasse aufrufen.



| IMediaObject-Methode                   | Abgeleitete Klassenmethode                                                             |
|---------------------------------------|----------------------------------------------------------------------------------|
| **GetInputCurrentType**               | Vollständig implementiert                                                                |
| **GetOutputCurrentType**              | Vollständig implementiert                                                                |
| **GetStreamCount**                    | Vollständig implementiert                                                                |
| **GetInputStatus**                    | [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))        |
| **Sperre** (implementiert als **DMOLock**) | [**Sperren,**](/previous-versions/ms809100(v=msdn.10)) [ **Entsperren**](/previous-versions/ms809101(v=msdn.10)) |
| **SetInputType**                      | [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))        |
| **SetOutputType**                     | [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IMediaObjectImpl-Klassenvorlage**](imediaobjectimpl-class-template.md)
</dt> <dt>

[Schreiben eines DMO](writing-a-dmo.md)
</dt> </dl>

 

 
