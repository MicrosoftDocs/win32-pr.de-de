---
description: Beschreibt, wie eine XPS OM initialisiert wird, mit der ein Programm ein XPS-Dokument erstellen kann.
ms.assetid: 920d940f-5ae2-4376-8c7b-0cef04f21df7
title: Initialisieren einer XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16edb992efee7c9cba1d5bc454ca5bcb44bd3267a2e91d4ca714120182df0657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119946992"
---
# <a name="initialize-an-xps-om"></a>Initialisieren einer XPS OM

Beschreibt, wie eine XPS OM initialisiert wird, mit der ein Programm ein XPS-Dokument erstellen kann.

Die Schnittstellen der XPS-Dokument-API werden von einer [**IXpsOMObjectFactory-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) erstellt. Rufen Sie [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)auf, um einen Zeiger auf eine **IXpsOMObjectFactory** abzurufen, die in Ihrem Programm verwendet werden kann.

Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss unter [Common XPS Document Programming Tasks (Allgemeine XPS-Dokumentprogrammierungsaufgaben).](common-xps-document-tasks.md)

## <a name="code-example"></a>Codebeispiel

Im folgenden Beispiel wird die Objektfactory erstellt, die zum Erstellen von XPS OM-Schnittstellen in anderen Beispielen verwendet wird.


```C++
    IXpsOMObjectFactory *xpsFactory;

    HRESULT hr = S_OK;

    // Init COM for this thread if it hasn't 
    //  been initialized, yet.
    hr = CoInitializeEx(0, COINIT_MULTITHREADED);

    hr = CoCreateInstance(
        __uuidof(XpsOMObjectFactory),
        NULL, 
        CLSCTX_INPROC_SERVER,
        __uuidof(IXpsOMObjectFactory),
        reinterpret_cast<LPVOID*>(&xpsFactory));

    if (SUCCEEDED(hr))
    {
        // Make sure that you got a pointer 
        //  to the interface.

        // Use object factory...

        // ... and release when done
        xpsFactory->Release();
    }

    // Uninitialize COM when finished
    CoUninitialize();
```



## <a name="best-practices"></a>Empfehlungen

Sie können ihr Programm effizienter gestalten, indem Sie einen Zeiger auf eine [**IXpsOMObjectFactory-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) abrufen, wenn Sie **IXpsOMObjectFactory** zum ersten Mal aufrufen müssen, um eine Schnittstelle zu erstellen, und dann den Zeiger für die Verwendung in anderen Bereichen des Programms speichern. Wenn das Programm die Objektfactory nicht mehr benötigt oder eine Weile nicht benötigt, kann der Zeiger freigegeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Erstellen eines leeren XPS OM](create-a-blank-xps-om.md)
</dt> <dt>

**Wird in diesem Abschnitt verwendet**
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Verpackung](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[REFERENZ ZUR XPS-Dokument-API](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
