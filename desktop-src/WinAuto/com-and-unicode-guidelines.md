---
title: COM- und Unicode-Richtlinien
description: Da Microsoft Active Accessibility auf Component Object Model (COM) basiert, benötigen Entwickler ein moderates Verständnis für COM-Objekte und -Schnittstellen und müssen wissen, wie grundlegende Aufgaben (z. B. initialisieren der COM-Bibliothek) auszuführen sind.
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023b1d58a1a31997142097d02d8fc7d80881111e08f0020d967c1984d9946c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133903"
---
# <a name="com-and-unicode-guidelines"></a>COM- und Unicode-Richtlinien

Da Microsoft Active Accessibility auf Component Object Model (COM) basiert, benötigen Entwickler ein moderates Verständnis für COM-Objekte und -Schnittstellen und müssen wissen, wie grundlegende Aufgaben (z. B. initialisieren der COM-Bibliothek) auszuführen sind. Serverentwickler müssen verstehen, wie Klassen erstellt werden, die die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementieren, und wie barrierefreie Objekte erstellt werden.

Sie benötigen auch ein mittleres Verständnis von Unicode, um viele der funktionen zu Microsoft Active Accessibility, die Zeichenfolgen zurückgeben.

Um die Microsoft Active Accessibility effektiv nutzen zu können, sollten Sie die folgenden COM- und Unicode-Funktionen, -Strukturen, -Datentypen und -Schnittstellen verstehen. Eingeschränkte Informationen zu einigen dieser Elemente finden Sie in dieser Dokumentation.

### <a name="functions"></a>Funktionen:

-   [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) oder [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
-   [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) und [ **IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)
-   [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) und [ **VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)
-   [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) und [ **WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
-   [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) und [ **SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)

### <a name="structures-and-data-types"></a>Strukturen und Datentypen:

-   [**Variante**](variant-structure.md)
-   [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)
-   [**Bstr**](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a>COM-Schnittstellen:

-   [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [**IDispatch**](idispatch-interface.md)
-   [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a>In diesem Abschnitt

-   [VARIANT-Struktur](variant-structure.md)
-   [IDispatch-Schnittstelle](idispatch-interface.md)
-   [Konvertieren von Unicode- und ANSI-Zeichenfolgen](converting-unicode-and-ansi-strings.md)

 

 