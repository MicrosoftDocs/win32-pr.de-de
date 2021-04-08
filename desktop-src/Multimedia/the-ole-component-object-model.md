---
title: Der OLE-Component Object Model
description: Der OLE-Component Object Model
ms.assetid: f3200d81-c2fa-4cc7-bf85-54f6c753a529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211c41de8c16eb1cabb1e62f475adbbf603e2c92
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "103949212"
---
# <a name="the-ole-component-object-model"></a>Der OLE-Component Object Model

Die von der avifile-Bibliothek verwendeten Objekte sind Teil der OLE-Component Object Model. Dies bedeutet hauptsächlich, dass Sie bestimmte Methoden gemeinsam nutzen, die Ihnen die Arbeit erleichtern, und die zurückgegebenen Werte gelten für die meisten OLE-Schnittstellen Methoden.

Der OLE-Component Object Model der Datei-und Datenstrom Handler verwendet die OLE **IClassFactory** -Schnittstelle, um Instanzen Ihrer Objektklasse zu erstellen. Als Komponenten Objekte implementieren Sie die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, die aus der [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void))-, [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)-und [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -Methode besteht. Mit der **IUnknown** -Schnittstelle kann eine Anwendung Zeiger auf andere Schnittstellen abrufen, die vom gleichen Objekt unterstützt werden.

Mithilfe der **QueryInterface** -Methode können Sie feststellen, ob ein Objekt eine bestimmte Schnittstelle unterstützt. Wenn ein Objekt eine angegebene Schnittstelle unterstützt, gibt **QueryInterface** einen Zeiger auf diese Schnittstelle zurück.

Sie können den Verweis Zähler, der einem Objekt zugeordnet ist, erhöhen und verringern, indem Sie die [**adressf**](/previous-versions//dd757100(v=vs.85)) -und [**releasemethoden**](/previous-versions//dd757102(v=vs.85)) verwenden. Der Verweis Zähler ermöglicht mehreren Clients den Zugriff auf ein Objekt. Wenn ein Objekt von der ersten Anwendung verwendet wird, wird der Verweis Zähler auf 1 festgelegt. Anwendungen verwenden anschließend die **adressf** -Methode, um die Anzahl zu erhöhen, damit das Objekt nachverfolgen kann, wie oft auf das Objekt zugegriffen wird.

Wenn eine Anwendung mithilfe eines Objekts ausgeführt wird, wird die **releasemethode** aufgerufen, um den Verweis Zähler zu Dekrementen. Wenn der Verweis Zähler Null ist, wird das Objekt nicht mehr benötigt, und das Release gibt alle Ressourcen **frei** , die es verwendet, und zerstört das-Objekt. Da ein Objekt interne Ressourcen verwendet, die für die Anwendung transparent sind, ist das-Objekt für die Freigabe verantwortlich. Beispielsweise kann es vorkommen, dass ein Datei Handler geöffnete Datenträger Dateien und freien Pufferspeicher bei der Freigabe schließt.

Die meisten OLE-Schnittstellen Methoden geben Ergebnis Handles zurück, die mithilfe des **HRESULT** -Datentyps definiert werden. Dieser Datentyp besteht aus einem Schweregrad Code, Kontextinformationen, einem Einrichtungs Code und einem Statuscode. Ein Rückgabe Ergebnis Handle, das angibt, dass der Wert 0 (null) ist. Ein Wert ungleich 0 (null) gibt einen Fehler an, und der Statuscode-Member des Rückgabe Ergebnis Handles stellt eine Grundlage für die zusätzliche Interpretation dar. Weitere Informationen zu OLE-Rückgabe Ergebnis Handles finden Sie in der *OLE-Programmier Referenz*.

 

 