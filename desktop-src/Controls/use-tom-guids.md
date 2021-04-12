---
title: Verwenden von Tom-GUIDs
description: Tom-GUIDs (Text Object Model) werden in "Tom. h" in den-Anweisungen der Mittell- \_ Schnittstelle angegeben. Um die zugeordneten Schnittstellen zu verwenden, müssen Sie zuerst die-Schnittstelle mit der GUID deklarieren.
ms.assetid: 48FF98C9-D42E-4E7F-874F-8E56F730E24E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c937d8b3c3612a3a49f27f18ac7c392b7a596
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "104472452"
---
# <a name="how-to-use-tom-guids"></a>Verwenden von Tom-GUIDs

Tom-GUIDs (Text Object Model) werden in "Tom. h" in den-Anweisungen der Mittell- \_ Schnittstelle angegeben. Um die zugeordneten Schnittstellen zu verwenden, müssen Sie zuerst die-Schnittstelle mit der GUID deklarieren.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="use-a-tom-guid"></a>Tom-GUID verwenden

Der folgende Beispielcode zeigt, wie die [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) -Schnittstelle verwendet wird.


```C++
#define DEFINE_GUIDXXX(name, l, w1, w2, b1, b2, b3, b4, b5, b6, b7, b8) \
        EXTERN_C const GUID CDECL name \
                = { l, w1, w2, { b1, b2,  b3,  b4,  b5,  b6,  b7,  b8 } }

DEFINE_GUIDXXX(IID_ITextDocument,0x8CC497C0,0xA1DF,0x11CE,0x80,0x98,
                0x00,0xAA,0x00,0x47,0xBE,0x5D);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Text Objektmodells](using-the-text-object-model.md)
</dt> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




