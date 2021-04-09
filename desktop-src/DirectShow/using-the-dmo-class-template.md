---
description: Verwenden der DMO-Klassen Vorlage
ms.assetid: 5193ad08-aaee-47e3-93eb-a126a66d8f23
title: Verwenden der DMO-Klassen Vorlage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db80017372f11f6c928e0e6a83b591967a84ee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042561"
---
# <a name="using-the-dmo-class-template"></a>Verwenden der DMO-Klassen Vorlage

DirectShow enthält eine Klassen Vorlage, [**imediaobjectimpl**](imediaobjectimpl-class-template.md), für die Implementierung von dmos. Die Vorlage behandelt viele der Buchhaltungsaufgaben, z. b. die Validierung von Eingabe Parametern. Mithilfe der Vorlage können Sie sich auf die Funktionen konzentrieren, die für Ihren DMO spezifisch sind. Außerdem hilft Ihnen die Vorlage dabei, sicherzustellen, dass Sie eine robuste Implementierung erstellen. Die Vorlage wird in der Header Datei "dmuimpl. h" definiert, die sich im Include-Verzeichnis des SDK befindet.

Die **imediaobjectimpl** -Vorlage erbt die [**imediaobject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) -Schnittstelle. Zum Erstellen eines DMO mithilfe der Vorlage definieren Sie eine neue Klasse, die von **imediaobjectimpl** abgeleitet ist. Die Vorlage implementiert alle **imediaobject** -Methoden. In den meisten Fällen ruft die Vorlage eine entsprechende private Methode für die abgeleitete Klasse auf. Die Vorlage bietet die folgenden Features:

-   Grundlegende Parameter Überprüfung. Die Vorlagen Methoden überprüfen, ob erforderliche Parameter nicht **null** sind, dass sich streamindizes innerhalb des Bereichs befinden und dass Flags gültig sind.
-   Gelungen. Mit den Vorlagen Methoden werden zwei interne Methoden, **Lock** und **Unlock**, aufgerufen, um Vorgänge für den DMO zu serialisieren. Mit dieser Funktion wird sichergestellt, dass das DMO Thread sicher ist.
-   Medientypen. In der Vorlage werden die vom Client festgelegten Medientypen gespeichert und Accessormethoden für die Medientypen bereitstellt.
-   -. Die Vorlage verhindert das Streaming, bis der Client Medientypen für alle nicht optionalen Streams festgelegt hat. Außerdem wird sichergestellt, dass die Methode [**imediaobject:: Zuordnungs**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) Methode aufgerufen wird, bevor das Streaming beginnt, wodurch sichergestellt wird, dass Ressourcen zugewiesen werden.

Die abgeleitete Klasse muss die **IUnknown** -Schnittstelle implementieren. Diese Schnittstelle wird von der Vorlage nicht bereitgestellt. Sie können die Active Template Library (ATL) verwenden, um **IUnknown** zu implementieren, oder Sie können eine andere Implementierung bereitstellen. Die Vorlage implementiert auch nicht den Sperrmechanismus. Die abgeleitete Klasse muss die **Lock** -und **Unlock** -Methoden implementieren. Wenn Sie die Klasse mithilfe von ATL erstellen, können Sie die standardmäßigen ATL-Implementierungen verwenden.

**Deklaration der abgeleiteten Klasse**

Die **imediaobjectimpl** -Klassen Vorlage wird wie folgt deklariert:


```C++
template <class _DERIVED_, int NUMBEROFINPUTS, int NUMBEROFOUTPUTS>
class IMediaObjectImpl : public ImediaObject
```



Die drei Vorlagen Parameter sind \_ abgeleitet \_ , "zahlofinputs" und "nummerierungsausgaben". \_Der abgeleitete Satz \_ entspricht dem Namen der Klasse. Mit den beiden anderen Parametern wird die Anzahl der Eingabedaten Ströme und der Ausgabedaten Ströme im DMO definiert. Verwenden Sie beispielsweise die folgende Deklaration, um eine DMO-Klasse mit dem Namen cmydmo zu erstellen, die einen Eingabedaten Strom und zwei Ausgabedaten Ströme unterstützt:


```C++
class CMyDmo : public IMediaObjectImpl<CMyDmo, 1, 2>
```



Im restlichen Teil dieses Abschnitts wird beschrieben, wie die verschiedenen Methoden in **imediaobject** von der Vorlage implementiert werden.

**Methoden zum Festlegen von Medientypen**

Die folgenden Methoden legen Medientypen im DMO fest oder rufen Sie ab:

-   **Getinputtype**, **getoutputtype**. Diese Methoden geben bevorzugte Medientypen nach streamnummer und Typindex zurück. Die Vorlage ruft **internalgetinputtype** oder **internalgetoutputtype** für die abgeleitete Klasse auf.
-   **Setinputtype**, **setoutputtype**. Diese Methoden legen den Medientyp für einen Stream fest, testen einen Medientyp oder löschen einen Medientyp. Um den Medientyp zu validieren, ruft die Vorlage **internalcheckinputtype** oder **internalcheckoutputtype** für die abgeleitete Klasse auf. Die abgeleitete Klasse gibt S \_ OK zurück, um den Typ oder DMO \_ E \_ invalidtype zu akzeptieren, um den Typ abzulehnen. Die Vorlage behandelt das Festlegen oder Löschen des Medientyps.
-   **Getinputcurrenttype**, **getoutputcurrenttype**. Diese Methoden geben den aktuellen Medientyp für einen Stream zurück, oder der DMO \_ E- \_ Typ \_ \_ wird nicht festgelegt, wenn kein Typ festgelegt ist. Diese Methoden werden von der Vorlage vollständig implementiert.

**Informationsmethoden**

Die folgenden Methoden stellen Informationen über den DMO bereit.

-   **Getinputmaxlatency**, * **tinputmaxlatency**. Mit diesen Methoden wird die maximale Latenzzeit abgerufen oder festgelegt. Die Vorlage ruft **internalgetinputmaxlatency** oder **internalsettinputmaxlatency** für die abgeleitete Klasse auf.
-   **Getinputsizone FO**, **getoutputsizone FO**. Diese Methoden geben die Puffer Anforderungen des DMO für einen angegebenen Stream zurück. Wenn kein Medientyp für diesen Stream festgelegt wurde, gibt die Vorlage den DMO \_ E- \_ Typ \_ nicht \_ festgelegt zurück. Andernfalls wird **internalgetinputsizone FO** oder **internalgetoutputsizone Info** für die abgeleitete Klasse aufgerufen.
-   **Getinputstreaminfo**, **getoutputstreaminfo**. Diese Methoden geben verschiedene Flags zurück, die angeben, wie der Client die Daten formatieren soll. Die Vorlage ruft **internalgetinputstreaminfo** oder **internalgetoutputstreaminfo** für die abgeleitete Klasse auf.
-   **Getstreamcount**. Diese Methode gibt die Anzahl von Eingabe-und Ausgabestreams zurück. Die Vorlage implementiert diese Methode mit den Vorlagen Parametern.

**Methoden für die Ressourcen Zuordnung**

-   Die Methode "Methode **zuweisen** " weist alle Ressourcen zu, die die DMO benötigt, bevor das Streaming beginnt. Die Methode " **freestreamingresources** " gibt dieselben Ressourcen frei. Die Vorlage ruft **internaldepaseestreamingresources** bzw. **internalfreestreamingresources** auf.

Der DMO-Client muss diese Methoden nicht aufrufen, aber die **Vorlage ruft vor** dem Streaming automatisch "" "" "". Daher kann der DMO davon ausgehen, dass Ressourcen ordnungsgemäß zugeordnet wurden, wenn **ProcessInput** aufgerufen wird. Der DMO sollte im Dekonstruktor " **freestreamingresources** " aufzurufen.

Wenn die Vorlage **internalzuzugestreamingresources** aufruft, legt Sie außerdem ein internes Flag fest, sodass diese Methode erst wieder aufgerufen wird, wenn **internalfreestreamingresources** aufgerufen wird. Dadurch wird sichergestellt, dass Ressourcen nicht versehentlich erneut zugewiesen werden, was zu Speicher Verlusten führen kann.

**Methoden für das Streaming**

Zum Streamen von Daten werden die folgenden Methoden verwendet:

-   **Getinputstatus**. Diese Methode gibt an, ob der DMO zu diesem Zeitpunkt Eingaben akzeptieren kann. Die Vorlage ruft **internalakzeptinginput** für die abgeleitete Klasse auf. Wenn der DMO Eingaben akzeptieren kann, gibt die abgeleitete Klasse "S OK" zurück, \_ und die Vorlage legt das DMO-Eingabe-Daten-Daten Satz- \_ Accept- \_ \_ \_ Daten Bit im *dwFlags* -Parameter fest. Andernfalls gibt die abgeleitete Klasse den Wert "false" zurück \_ , und die Vorlage legt *dwFlags* auf NULL fest.
-   **ProcessInput**. Diese Methode verarbeitet einen Eingabepuffer. Die **Vorlage ruft "**" "" "" "" "" "". Anschließend wird **internalakzeptinginput** für die abgeleitete Klasse aufgerufen. Wenn der DMO neue Eingaben akzeptieren kann, ruft die Vorlage **internalprocessinput** auf.
-   **ProcessOutput**. Diese Methode verarbeitet einen Satz von Ausgabe Puffern, einen Puffer für jeden Ausgabestream. Die Vorlage ruft " **depaseestreamingresources** " und dann " **internalprocessoutput**" auf.
-   **Diskontinuität**. Diese Methode signalisiert eine Diskontinuität in einem Eingabedaten Strom. Die Vorlage ruft **internalakzeptinginput** für die abgeleitete Klasse auf. Wenn diese Methode S OK zurückgibt \_ , ruft die Vorlage **internaldiscontinuity** für die abgeleitete Klasse auf.
-   Leeren. Diese Methode leert den DMO. Die Vorlage ruft **internalflush** für die abgeleitete Klasse auf. Der DMO sollte alle Eingabepuffer verwerfen, die noch verarbeitet werden sollen.

Die Vorlage bietet keine direkte Unterstützung für die [**imediaobjectinplace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) -Schnittstelle.

**Methoden zum Sperren**

Sperren werden verwendet, um den Status von DMO in einer Multithread-Umgebung zu schützen. In einem ATL-Projekt verursacht die [**imediaobject:: Lock**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-lock) -Methode einen namens Konflikt mit der ATL- **Sperr** Methode. Um den Konflikt aufzulösen, benennt die Vorlage die **imediaobject** -Methode in **dmolock** um. Wenn Sie die abgeleitete Klasse kompilieren, definieren \_ Sie \_ den Namen der fixsperre, bevor Sie die Header Datei "DMO. h" einschließen:


```C++
#define FIX_LOCK_NAME
#include <dmo.h>
```



Diese Direktive bewirkt, dass der Präprozessor **dmolock** zur **Sperre** in der Deklaration der **imediaobject** -Schnittstelle ersetzt. Anwendungen können die Methode weiterhin mithilfe der namens **Sperre** aufrufen, da sich die Vtable-Reihenfolge nicht ändert. Die **dmolock** -Methode ruft **Lock** oder **Unlock** für die abgeleitete Klasse auf. Wenn Sie ATL verwenden, um die abgeleitete Klasse zu implementieren, werden diese Methoden bereits von ATL definiert, sodass kein zusätzlicher Code erforderlich ist. Wenn Sie ATL nicht verwenden, müssen Sie in der abgeleiteten Klasse **Lock** -und **Unlock** -Methoden bereitstellen.

Die Vorlage sperrt den DMO automatisch in jeder der **imediaobject** -Methoden. Die abgeleitete Klasse muss möglicherweise den DMO in anderen öffentlichen Methoden sperren, die Sie implementiert (z. b. Wenn Sie **imediaobjectinplace** unterstützt). Die Klassen Vorlage bietet auch eine interne Hilfsklasse, [**imediaobjectimpl:: LockIT**](imediaobjectimpl-lockit.md), die zum Sperren und Entsperren des DMO nützlich ist.

**Zusammenfassung**

Für die folgenden **imediaobject** -Methoden Ruft die Vorlage eine entsprechende Methode mit derselben Signatur in der abgeleiteten Klasse auf. Die abgeleitete Klasse muss jede der in der zweiten Spalte gezeigten Methoden implementieren.



| Imediaobject-Methode            | Methode der abgeleiteten Klasse                   |
|--------------------------------|----------------------------------------|
| **"" Zugeordnet** | **Internaldeperestreamingresources** |
| **Diskontinuität**              | **Internaldiscontinuity**              |
| **Leerung**                      | **Internalflush**                      |
| **Freestreamingresources**     | **Internalfreestreamingresources**     |
| **Getinputmaxlatency**         | **Internalgetinputmaxlatency**         |
| **Getinputsizone FO**           | **Internalgetinputsizone FO**           |
| **Getinputstreaminfo**         | **Internalgetinputstreaminfo**         |
| **Getinputtype**               | **Internalgetinputtype**               |
| **Getoutputsizone FO**          | **Internalgetoutputsizone FO**          |
| **Getoutputstreaminfo**        | **Internalgetoutputstreaminfo**        |
| **Getoutputtype**              | **Internalgetoutputtype**              |
| **ProcessInput**               | **Internalprocessinput**               |
| **ProcessOutput**              | **Internalprocessoutput**              |
| **"* Tinputmaxlatency"**         | **Internal* tinputmaxlatency**         |



 

Für die verbleibenden **imediaobject** -Methoden gibt es keine eins-zu-eins-Entsprechung zwischen Vorlagen Methoden und Methoden für abgeleitete Klassen. In der folgenden Tabelle ist zusammengefasst, welche Methoden von der Vorlage vollständig implementiert werden und welche Methoden andere Methoden in der abgeleiteten Klasse aufzurufen.



| Imediaobject-Methode                   | Methode der abgeleiteten Klasse                                                             |
|---------------------------------------|----------------------------------------------------------------------------------|
| **Getinputcurrenttype**               | Vollständig implementiert                                                                |
| **Getoutputcurrenttype**              | Vollständig implementiert                                                                |
| **Getstreamcount**                    | Vollständig implementiert                                                                |
| **Getinputstatus**                    | [**Internalakzeptinginput**](/previous-versions/ms809095(v=msdn.10))        |
| **Lock** (implementiert als **dmolock**) | [**Sperren**](/previous-versions/ms809100(v=msdn.10)), [ **entsperren**](/previous-versions/ms809101(v=msdn.10)) |
| **"Ttinputtype"**                      | [**Internalcheckinputtype**](/previous-versions/ms809096(v=msdn.10))        |
| **Setoutputtype**                     | [**Internalcheckoutputtype**](/previous-versions/ms809098(v=msdn.10))      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Imediaobjectimpl-Klassen Vorlage**](imediaobjectimpl-class-template.md)
</dt> <dt>

[Schreiben eines DMO](writing-a-dmo.md)
</dt> </dl>

 

 
