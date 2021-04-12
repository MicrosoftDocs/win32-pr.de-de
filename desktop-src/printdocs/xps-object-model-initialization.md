---
description: Beschreibt, wie ein XPS-OM initialisiert wird, das einem Programm das Erstellen eines XPS-Dokuments ermöglicht.
ms.assetid: 920d940f-5ae2-4376-8c7b-0cef04f21df7
title: Initialisieren eines XPS-OMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac44a69d171c1d38633512b0e275dcdeaea8738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344829"
---
# <a name="initialize-an-xps-om"></a>Initialisieren eines XPS-OMS

Beschreibt, wie ein XPS-OM initialisiert wird, das einem Programm das Erstellen eines XPS-Dokuments ermöglicht.

Die Schnittstellen der XPS-Dokument-API werden von einer [**ixpsomobjectfactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) -Schnittstelle erstellt. Rufen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)auf, um einen Zeiger auf eine **ixpsomobjectfactory** zu erhalten, die in Ihrem Programm verwendet werden kann.

Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Allgemeine XPS-Dokument Programmieraufgaben](common-xps-document-tasks.md).

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



## <a name="best-practices"></a>Bewährte Methoden

Sie können Ihr Programm effizienter gestalten, indem Sie einen Zeiger auf eine [**ixpsomobjectfactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) -Schnittstelle erhalten, wenn Sie zum ersten Mal **ixpsomobjectfactory** aufrufen müssen, um eine Schnittstelle zu erstellen, und dann den Zeiger für die Verwendung in anderen Bereichen des Programms speichern. Wenn das Programm die Objektfactory nicht mehr benötigt oder es für eine Weile nicht benötigt, kann der Zeiger freigegeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Erstellen eines leeren XPS-OMS](create-a-blank-xps-om.md)
</dt> <dt>

**In diesem Abschnitt verwendet**
</dt> <dt>

[**Ixpsomobjectfactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Verpackung](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XPS-Dokument-API-Referenz](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
