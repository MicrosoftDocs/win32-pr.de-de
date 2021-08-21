---
title: Ole-Component Object Model
description: Ole-Component Object Model
ms.assetid: f3200d81-c2fa-4cc7-bf85-54f6c753a529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de83641250c912efbe92d7181deb52b477af06e2b49598ee63762488a932687
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805020"
---
# <a name="the-ole-component-object-model"></a>Ole-Component Object Model

Die von der AVIFile-Bibliothek verwendeten Objekte sind alle Teil des OLE-Component Object Model. Dies bedeutet in erster Linie, dass sie bestimmte Methoden gemeinsam nutzen, mit denen sie einfacher zu arbeiten sind, und die zurückgegebenen Werte sind für die meisten OLE-Schnittstellenmethoden üblich.

Der OLE-Component Object Model der Datei- und Streamhandler verwendet die OLE **IClassFactory-Schnittstelle,** um Instanzen ihrer Objektklasse zu erstellen. Als Komponentenobjekte implementieren sie die [IUnknown-Schnittstelle,](/windows/win32/api/unknwn/nn-unknwn-iunknown) die aus den Methoden [**QueryInterface,**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)) [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)und [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) besteht. Mit der **IUnknown-Schnittstelle** kann eine Anwendung Zeiger auf andere Schnittstellen abrufen, die vom gleichen Objekt unterstützt werden.

Mithilfe der **QueryInterface-Methode** können Sie ermitteln, ob ein Objekt eine bestimmte Schnittstelle unterstützt. Wenn ein Objekt eine angegebene Schnittstelle unterstützt, gibt **QueryInterface** einen Zeiger auf diese Schnittstelle zurück.

Sie können den einem Objekt zugeordneten Verweiszähler mithilfe der Methoden [**AddRef**](/previous-versions//dd757100(v=vs.85)) und [**Release**](/previous-versions//dd757102(v=vs.85)) erhöhen und dekrementieren. Mit der Verweisanzahl können mehrere Clients auf ein Objekt zugreifen. Wenn ein Objekt von der ersten Anwendung verwendet wird, wird dessen Verweisanzahl auf 1 festgelegt. Anwendungen verwenden anschließend die **AddRef-Methode,** um die Anzahl zu erhöhen, damit das Objekt nachverfolgen kann, wie oft darauf zugegriffen wird.

Wenn eine Anwendung mit einem -Objekt fertig ist, ruft sie die **Release-Methode** auf, um den Verweiszähler zu dekrementieren. Wenn der Verweiszähler 0 (null) ist, wird das Objekt nicht mehr benötigt, und **Release** gibt alle verwendeten Ressourcen frei und zerstört das Objekt. Da ein Objekt interne Ressourcen verwendet, die für die Anwendung transparent sind, ist das Objekt dafür verantwortlich, sie frei zu machen. Ein Dateihandler muss z. B. geöffnete Datenträgerdateien schließen und Pufferspeicher freigeben, wenn er freigegeben wird.

Die meisten OLE-Schnittstellenmethoden geben Ergebnishandles zurück, die mit dem **HRESULT-Datentyp** definiert werden. Dieser Datentyp besteht aus einem Schweregradcode, Kontextinformationen, einem Einrichtungscode und einem Statuscode. Ein Rückgabeergebnishandle, das angibt, dass erfolgreich ist, hat den Wert 0 (null). Ein Wert ungleich 0 (null) gibt einen Fehler an, und der Statuscodemember des Rückgabeergebnishandle stellt eine Grundlage für zusätzliche Interpretationen bereit. Weitere Informationen zu OLE-Rückgabeergebnishandles finden Sie in der *Referenz des OLE-Programmierers.*

 

 