---
title: Die com-Bibliothek
description: Die com-Bibliothek
ms.assetid: 51d4db4a-ad88-4627-8140-2f7906945752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a285a89ca659907c37f92b7d00f3e3e04d0acf51
ms.sourcegitcommit: 307b14e9847ced354a52a1ac12d7f659722d99bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2020
ms.locfileid: "103948493"
---
# <a name="the-com-library"></a>Die com-Bibliothek

Jeder Prozess, der com verwendet, muss die com-Bibliothek initialisieren und die Initialisierung der com-Bibliothek deaktivieren. Zusätzlich zu einer Spezifikation implementiert com auch einige wichtige Dienste in dieser Bibliothek. Die com-Bibliothek bietet Folgendes als einen Satz von DLLs und EXEs (Primär Ole32.dll und Rpcss.exe) in Microsoft Windows:

-   Eine kleine Anzahl grundlegender Funktionen, die die Erstellung von com-Anwendungen vereinfachen, sowohl Client als auch Server. Für-Clients stellt com grundlegende Funktionen zum Erstellen von-Objekten bereit. Bei-Servern bietet com die Möglichkeit, Ihre Objekte verfügbar zu machen.

-   Implementierungs-Locator-Dienste, über die com von einem eindeutigen Klassen Bezeichner (CLSID) bestimmt, welcher Server diese Klasse implementiert und wo sich der Server befindet. Dieser Dienst umfasst Unterstützung für eine dereferenzierungsstufe, normalerweise eine Systemregistrierung, zwischen der Identität einer Objektklasse und der Verpackung der Implementierung, sodass Clients unabhängig von der Verpackung sind, die sich in der Zukunft ändern können.

-   Transparente Remote Prozedur Aufrufe, wenn ein Objekt auf einem lokalen Server oder Remote Server ausgeführt wird.

-   Ein Standardmechanismus, mit dem eine Anwendung steuern kann, wie der Arbeitsspeicher innerhalb des Prozesses zugewiesen wird. Dies gilt insbesondere für Arbeitsspeicher, der zwischen den zusammengesetzten Objekten übermittelt werden muss, damit Sie ordnungsgemäß freigegeben werden

Um grundlegende COM-Dienste verwenden zu können, müssen alle com-Threads der Ausführung in Clients und Prozess externen Servern entweder die [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) -Funktion oder die [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) -Funktion aufrufen, bevor Sie eine andere com-Funktion außer Speicher Belegungs aufrufen aufrufen können. **CoInitializeEx** ersetzt die andere Funktion und fügt einen Parameter hinzu, der es Ihnen ermöglicht, das Threading Modell des Threads anzugeben: entweder Apartment Thread oder frei Thread. Durch einen **CoInitialize** -Rückruf wird das Threading Modell einfach auf Apartment Thread festgelegt.

OLE-Verbund Dokument Anwendungen rufen die [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) -Funktion auf, die [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) aufruft und auch einige für Verbund Dokumente erforderliche Initialisierung durchführt. Daher können Threads, die **OleInitialize** aufzurufen, nicht freigegeben werden. Weitere Informationen zum Threading in Clients und Servern finden Sie unter [Prozesse, Threads und Apartments](processes--threads--and-apartments.md).

Prozess interne Server nennen die Initialisierungs Funktionen nicht, da Sie in einen Prozess geladen werden, der bereits abgeschlossen ist. Daher müssen Prozess interne Server Ihr Threading Modell in der Registrierung unter dem Schlüssel [InProcServer32](inprocserver32.md) festlegen. Ausführliche Informationen zu Threading Problemen bei Prozess internen Servern finden Sie unter [Prozess interne Server Threading Probleme](in-process-server-threading-issues.md).

Es ist auch wichtig, die Initialisierung der Bibliothek zu deaktivieren. Für jeden Aufrufen von [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) oder [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)muss ein entsprechender [**CallInitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize)-Befehl vorhanden sein. Für jeden Aufrufe von [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize)muss ein entsprechender [**etuninitialize**](/windows/desktop/api/Ole2/nf-ole2-oleuninitialize)-aufrufswert vorhanden sein.

Prozess interne Server können davon ausgehen, dass der Prozess, in den Sie geladen werden, diese Schritte bereits ausgeführt hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Component Object Model](the-component-object-model.md)
</dt> </dl>

 

 




