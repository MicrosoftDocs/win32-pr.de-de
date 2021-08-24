---
title: Fragen eines Objekts nach einer Schnittstelle
description: Fragen eines Objekts nach einer Schnittstelle
ms.assetid: 04296372-4897-426e-9be3-e6862a530ac6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a173342c7dba59c09cdef05c6b20d9d4d37da9d6971e6a7c26c1787b708121bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680739"
---
# <a name="asking-an-object-for-an-interface"></a>Fragen eines Objekts nach einer Schnittstelle

Wir haben bereits gesehen, dass ein Objekt mehrere Schnittstellen implementieren kann. Das Common Item Dialog-Objekt ist ein praxisorientiertes Beispiel dafür. Um die typischen Verwendungen zu unterstützen, implementiert das -Objekt die [**IFileOpenDialog-Schnittstelle.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) Diese Schnittstelle definiert grundlegende Methoden zum Anzeigen des Dialogfelds und abrufen von Informationen über die ausgewählte Datei. Für eine erweiterte Verwendung implementiert das -Objekt jedoch auch eine Schnittstelle mit dem Namen [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize). Ein Programm kann diese Schnittstelle verwenden, um die Darstellung und das Verhalten des Dialogfelds anzupassen, indem es neue Ui-Steuerelemente hinzufügt.

Denken Sie daran, dass jede COM-Schnittstelle direkt oder indirekt von der [**IUnknown-Schnittstelle erben**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) muss. Das folgende Diagramm zeigt die Vererbung des Common Item Dialog-Objekts.

![Diagramm mit Schnittstellen, die vom allgemeinen Elementdialogobjekt verfügbar gemacht werden](images/com06.png)

Wie Sie im Diagramm sehen können, ist der direkte Vorgänger von [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) die [**IFileDialog-Schnittstelle,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) die wiederum [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow)erbt. Wenn Sie die Vererbungskette von **IFileOpenDialog** zu **IModalWindow** hochfahren, definieren die Schnittstellen zunehmend generalisierte Fensterfunktionen. Schließlich erbt die **IModalWindow-Schnittstelle** [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) Das Common Item Dialog-Objekt implementiert auch [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize), das in einer separaten Vererbungskette vorhanden ist.

Angenommen, Sie verfügen über einen Zeiger auf die [**IFileOpenDialog-Schnittstelle.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) Wie würden Sie einen Zeiger auf die [**IFileDialogCustomize-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) erhalten?

![Diagramm, das zwei Schnittstellenzeiger auf Schnittstellen für dasselbe Objekt zeigt](images/com07.png)

Das einfache Umwandeln des [**IFileOpenDialog-Zeigers**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) in einen [**IFileDialogCustomize-Zeiger**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) funktioniert nicht. Es gibt keine zuverlässige Möglichkeit, die Umwandlung über eine Vererbungshierarchie hinweg zu "kreuzen", ohne eine Form von Laufzeittypinformationen (RTTI), die ein stark sprachabhängiges Feature ist.

Der COM-Ansatz besteht darin, das -Objekt *aufzufordern,* Ihnen einen [**IFileDialogCustomize-Zeiger**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) zu geben, wobei die erste Schnittstelle als Verbindung mit dem Objekt verwendet wird. Dazu wird die [**IUnknown::QueryInterface-Methode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) vom ersten Schnittstellenzeiger aufgerufen. Sie können sich **QueryInterface** als sprachunabhängige Version des **Schlüsselworts dynamic \_ cast** in C++ vorstellen.

Die [**QueryInterface-Methode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) verfügt über die folgende Signatur:

``` syntax
HRESULT QueryInterface(REFIID riid, void **ppvObject);
```

Basierend auf dem, was Sie bereits über [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)wissen, können Sie möglicherweise erraten, wie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) funktioniert.

-   Der *riid-Parameter* ist die GUID, die die gewünschte Schnittstelle identifiziert. Der Datentyp **REFIID** ist eine **Typedef** für `const GUID&` . Beachten Sie, dass der Klassenbezeichner (CLSID) nicht erforderlich ist, da das Objekt bereits erstellt wurde. Nur der Schnittstellenbezeichner ist erforderlich.
-   Der *ppvObject-Parameter* empfängt einen Zeiger auf die Schnittstelle. Der Datentyp dieses Parameters ist **\* \* void,** aus demselben Grund, aus dem [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) diesen Datentyp verwendet: [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) kann zum Abfragen einer beliebigen COM-Schnittstelle verwendet werden, sodass der Parameter nicht stark typisiert werden kann.

So rufen Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, um einen [**IFileDialogCustomize-Zeiger**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) abzurufen:


```C++
hr = pFileOpen->QueryInterface(IID_IFileDialogCustomize, 
    reinterpret_cast<void**>(&pCustom));
if (SUCCEEDED(hr))
{
    // Use the interface. (Not shown.)
    // ...

    pCustom->Release();
}
else
{
    // Handle the error.
}
```



Überprüfen Sie wie  immer den HRESULT-Rückgabewert, falls die Methode fehlschlägt. Wenn die Methode erfolgreich ist, müssen Sie [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) aufrufen, wenn Sie mit dem Zeiger fertig sind, wie unter [Verwalten der Lebensdauer eines Objekts](managing-the-lifetime-of-an-object.md)beschrieben.

## <a name="next"></a>Nächste

[Speicherbelegung in COM](memory-allocation-in-com.md)

 

 