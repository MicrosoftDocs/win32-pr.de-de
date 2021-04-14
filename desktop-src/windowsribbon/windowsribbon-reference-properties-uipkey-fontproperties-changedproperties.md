---
title: UI_PKEY_FontProperties_ChangedProperties
description: Gibt die Benutzeroberflächen- \_ pkey \_ fontproperties \_ changedproperties-Eigenschaft an.
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124b36d5e24f4e0c0122cffdbbed11669a4ea510
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390769"
---
# <a name="ui_pkey_fontproperties_changedproperties"></a>UI \_ pkey \_ fontproperties \_ changedproperties

Gibt die Benutzeroberflächen- \_ pkey \_ fontproperties \_ changedproperties-Eigenschaft an.

```
propertyDescription
   name = UI_PKEY_FontProperties_ChangedProperties
   shellPKey = UI_PKEY_FontProperties_ChangedProperties
   formatID = 00000312-7363-696e-8441798acf5aebb7
   propID = 13
   typeInfo
      type = IUISimplePropertySet
```

## <a name="remarks"></a>Bemerkungen

UI \_ pkey \_ fontproperties \_ changedproperties wird von einer Anwendung verwendet, um nur geänderte Eigenschaften aus [UI \_ pkey \_ fontproperties](windowsribbon-reference-properties-uipkey-fontproperties.md)abzufragen.

Beim Aufrufen der [**iuisimplepropertyset:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) -Methode für dieses [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) -Objekt wird ein [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore)zurückgegeben.

UI \_ pkey \_ fontproperties \_ changedproperties wird als letzter Parameter des [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Aufrufes an die Menüband-Host Anwendung übergeben.

Dieser Eigenschafts Schlüssel ist schreibgeschützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schriftart Steuerelement-Eigenschaften](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**Iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 