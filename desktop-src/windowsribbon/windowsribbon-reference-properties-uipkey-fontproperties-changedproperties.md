---
title: UI_PKEY_FontProperties_ChangedProperties
description: Identifiziert die \_ PKEY \_ FontProperties \_ ChangedProperties-Eigenschaft der Benutzeroberfläche.
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36262a9acf217e448956f108b68cb0716b5b5080c71f6a2a8e305c9e59478c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028658"
---
# <a name="ui_pkey_fontproperties_changedproperties"></a>UI \_ PKEY \_ FontProperties \_ ChangedProperties

Identifiziert die \_ PKEY \_ FontProperties \_ ChangedProperties-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_FontProperties_ChangedProperties
   shellPKey = UI_PKEY_FontProperties_ChangedProperties
   formatID = 00000312-7363-696e-8441798acf5aebb7
   propID = 13
   typeInfo
      type = IUISimplePropertySet
```

## <a name="remarks"></a>Hinweise

Ui \_ PKEY \_ FontProperties \_ ChangedProperties wird von einer Anwendung verwendet, um nur geänderte Eigenschaften von [UI \_ PKEY \_ FontProperties abzufragen.](windowsribbon-reference-properties-uipkey-fontproperties.md)

Durch Aufrufen der [**IUISimplePropertySet::GetValue-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) für dieses [**IUISimplePropertySet-Objekt**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) wird ein [IPropertyStore-Objekt](/windows/win32/api/propsys/nn-propsys-ipropertystore)zurückgegeben.

Ui \_ PKEY \_ FontProperties \_ ChangedProperties wird als letzter Parameter des [**IUICommandHandler::Execute-Aufrufs**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) an die Menübandhostanwendung übergeben.

Dieser Eigenschaftsschlüssel ist schreibgeschützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftartsteuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[Schriftartsteuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 