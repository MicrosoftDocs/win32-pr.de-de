---
title: Anfordern eines Objekts für eine Schnittstelle
description: Anfordern eines Objekts für eine Schnittstelle
ms.assetid: 04296372-4897-426e-9be3-e6862a530ac6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fa740f0ef770e069ee03b644bbfcb9b2c5e0eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038999"
---
# <a name="asking-an-object-for-an-interface"></a>Anfordern eines Objekts für eine Schnittstelle

Wir haben bereits gesehen, dass ein Objekt mehr als eine Schnittstelle implementieren kann. Das allgemeine Element Dialogfeld Objekt ist ein reales Beispiel dafür. Zur Unterstützung der typischen Verwendungen implementiert das-Objekt die [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) -Schnittstelle. Diese Schnittstelle definiert grundlegende Methoden zum Anzeigen des Dialog Felds und zum erhalten von Informationen zur ausgewählten Datei. Für eine erweiterte Verwendung implementiert das Objekt jedoch auch eine Schnittstelle mit dem Namen [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize). Ein Programm kann diese Schnittstelle verwenden, um die Darstellung und das Verhalten des Dialog Felds anzupassen, indem neue UI-Steuerelemente hinzugefügt werden.

Denken Sie daran, dass jede com-Schnittstelle direkt oder indirekt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle geerbt werden muss. Das folgende Diagramm zeigt die Vererbung des Dialog Objekts für allgemeine Elemente.

![Diagramm, das Schnittstellen anzeigt, die vom Dialog Objekt für allgemeine Elemente verfügbar gemacht](images/com06.png)

Wie Sie im Diagramm sehen können, ist der direkte Vorgänger von [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) die [**ifiledialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) -Schnittstelle, die wiederum [**imodalwindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow)erbt. Wenn Sie die Vererbungs Kette von **IFileOpenDialog** zu **imodalwindow** aufrufen, definieren die Schnittstellen eine zunehmend verallgemeinerte Fenster Funktionalität. Schließlich erbt die **imodalwindow** -Schnittstelle [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). Das Common Item Dialog-Objekt implementiert auch [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize), das in einer separaten Vererbungs Kette vorhanden ist.

Angenommen, Sie verfügen über einen Zeiger auf die [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) -Schnittstelle. Wie erhalten Sie einen Zeiger auf die Schnittstelle [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) ?

![Diagramm, das zwei Schnittstellen Zeiger auf Schnittstellen für dasselbe Objekt anzeigt](images/com07.png)

Das einfache Umwandeln des [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) -Zeigers in einen [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) -Zeiger funktioniert nicht. Es gibt keine zuverlässige Möglichkeit, eine Kreuz Umwandlung über eine Vererbungs Hierarchie hinweg durchzuführen, ohne eine Form von Lauf Zeittyp Informationen (RTTI), bei der es sich um eine stark sprachabhängige Funktion handelt.

Der com-Ansatz besteht darin, das Objekt zu *bitten* , Ihnen einen [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) -Zeiger zu senden, wobei die erste Schnittstelle als Kanal für das Objekt verwendet wird. Dies erfolgt durch Aufrufen der [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode aus dem ersten Schnittstellen Zeiger. Sie können **QueryInterface** als sprachunabhängige Version des **Dynamic \_ Cast** -Schlüssel Worts in C++ betrachten.

Die [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode hat die folgende Signatur:

``` syntax
HRESULT QueryInterface(REFIID riid, void **ppvObject);
```

Basierend auf dem, was Sie bereits über [**copurateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)wissen, können Sie möglicherweise erraten, wie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) funktioniert.

-   Der *riid* -Parameter ist die GUID, die die Schnittstelle identifiziert, nach der Sie gefragt werden. Die Datentyp- **refi-ID** ist eine **typedef** für `const GUID&` . Beachten Sie, dass der Klassen Bezeichner (CLSID) nicht erforderlich ist, da das Objekt bereits erstellt wurde. Nur der Schnittstellen Bezeichner ist erforderlich.
-   Der *ppvobject* -Parameter erhält einen Zeiger auf die-Schnittstelle. Der Datentyp dieses Parameters ist **ungültig \* \***, aus demselben Grund, aus dem [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) diesen Datentyp verwendet: [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) kann verwendet werden, um eine beliebige com-Schnittstelle abzufragen, sodass der Parameter nicht stark typisiert werden kann.

Hier sehen Sie, wie Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) zum Abrufen eines [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) -Zeigers aufzurufen:


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



Überprüfen Sie wie immer den **HRESULT** -Rückgabewert, falls die Methode fehlschlägt. Wenn die Methode erfolgreich ausgeführt wird, müssen Sie [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) aufzurufen, wenn Sie den-Zeiger verwendet haben, wie unter [Verwalten der Lebensdauer eines Objekts](managing-the-lifetime-of-an-object.md)beschrieben.

## <a name="next"></a>Nächste

[Speicher Belegung in com](memory-allocation-in-com.md)

 

 