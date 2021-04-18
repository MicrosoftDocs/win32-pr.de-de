---
title: COM-und Unicode-Richtlinien
description: Da Microsoft Active Accessibility auf Component Object Model (com) basiert, benötigen Entwickler ein mittleres Maß an Kenntnissen über COM-Objekte und-Schnittstellen, und Sie müssen wissen, wie Sie grundlegende Aufgaben ausführen (z. b. die Initialisierung der com-Bibliothek).
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2312b6177891c31c0987b846f7adfc1aa08abc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338269"
---
# <a name="com-and-unicode-guidelines"></a>COM-und Unicode-Richtlinien

Da Microsoft Active Accessibility auf Component Object Model (com) basiert, benötigen Entwickler ein mittleres Maß an Kenntnissen über COM-Objekte und-Schnittstellen, und Sie müssen wissen, wie Sie grundlegende Aufgaben ausführen (z. b. die Initialisierung der com-Bibliothek). Server Entwickler müssen wissen, wie Klassen entworfen werden, die die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle implementieren, und wie barrierefreie Objekte erstellt werden.

Außerdem benötigen Sie ein mittleres Maß an Verständnis von Unicode, um viele der Funktionen von Microsoft Active Accessibility zu verwenden, die Zeichen folgen zurückgeben.

Um Microsoft Active Accessibility effektiv zu verwenden, sollten Sie die folgenden com-und Unicode-Funktionen, Strukturen, Datentypen und Schnittstellen kennen. Informationen zu einigen dieser Elemente finden Sie in dieser Dokumentation.

### <a name="functions"></a>Funktionen:

-   [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) oder [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
-   [**IUnknown:: adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) und [ **IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)
-   [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) und [ **VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)
-   " [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) " und " [ **WideCharToMultiByte** "](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
-   " [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) " und " [ **sysfrestring** "](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)

### <a name="structures-and-data-types"></a>Strukturen und Datentypen:

-   [**Konfigur**](variant-structure.md)
-   [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)
-   [**BSTR**](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a>COM-Schnittstellen:

-   [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [**IDispatch**](idispatch-interface.md)
-   [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a>In diesem Abschnitt

-   [VARIANT-Struktur](variant-structure.md)
-   [IDispatch-Schnittstelle](idispatch-interface.md)
-   [Unicode und ANSI-Zeichen folgen werden umgerechnet](converting-unicode-and-ansi-strings.md)

 

 