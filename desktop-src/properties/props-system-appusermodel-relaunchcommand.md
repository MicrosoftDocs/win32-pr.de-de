---
description: Gibt einen Befehl an, der über ShellExecute ausgeführt werden kann, um eine Anwendung zu starten, wenn sie an die Taskleiste angeheftet wird oder wenn eine neue Instanz der Anwendung über die Sprungliste der Anwendung gestartet wird.
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: System.AppUserModel.NeustartCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc2ce3783aa9ab3d76124b8d62f9d9d9ad2e1f5d4b92622716df111456dbabd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554520"
---
# <a name="systemappusermodelrelaunchcommand"></a>System.AppUserModel.NeustartCommand

Gibt einen Befehl an, der über [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) ausgeführt werden kann, um eine Anwendung zu starten, wenn sie an die Taskleiste angeheftet wird oder wenn eine neue Instanz der Anwendung über die Sprungliste der Anwendung gestartet wird.

Einige Beispiele dafür sind:


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



Diese Eigenschaft wird nur verwendet, wenn ein Fenster über eine explizite Anwendungsbenutzermodell-ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), festgelegt über [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)) verfügt. Wenn das Fenster nicht über eine explizite AppUserModelID verfügt, wird diese Eigenschaft ignoriert, und das Fenster wird gruppiert und angeheftet, als wäre es Teil des Prozesses, der es besitzt. Weitere Informationen zur Anwendung expliziter AppUserModelIDs und deren Auswirkungen auf das Anheften auf die Taskleiste finden Sie unter [Anwendungsbenutzermodell-IDs (AppUserModelIDs).](../shell/appids.md)

Diese Eigenschaft soll von Anwendungen oder Fenstern verwendet werden, die nicht standardmäßige Neustartinformationen bereitstellen möchten.

> [!Note]  
> [System.AppUserModel.NeustartCommand]() und [System.AppUserModel.NeustartDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) müssen immer zusammen festgelegt werden. Wenn eine dieser Eigenschaften nicht festgelegt ist, wird keine dieser Eigenschaften verwendet.

 

Diese Eigenschaft kann zusammen mit [System.AppUserModel.UsernameDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) und [System.AppUserModel.IconResource](./props-system-appusermodel-relaunchiconresource.md) verwendet werden, um ein Fenster visuell als Anwendung für den Benutzer zu definieren. Dies ist nützlich für Hostanwendungsszenarien, in denen eine einzelne Hostinstanz mehrere untergeordnete Anwendungen ausführt. Beispielsweise könnte ein virtueller Computer, der mehrere virtualisierte Anwendungen hostet, möchten, dass diese virtualisierten Anwendungen dem Benutzer als einzelne Anwendungen angezeigt werden. Der virtuelle Computer kann jedes Fenster mit einer expliziten AppUserModelID und den entsprechenden Neustarteigenschaften bezeichnen, damit sie als Anwendungen angezeigt werden. Der Benutzer kann sie dann an die Taskleiste anheften und die angeheftete Instanz "neu starten".

> [!Note]  
> Diese Eigenschaft wird ignoriert, wenn [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) festgelegt ist. Dadurch kann eine Anwendung die Gruppierung ihrer Fenster steuern, indem sie ihnen explizite AppUserModelIDs zuweist, aber verhindert, dass diese Fenster angeheftet werden.

 

Um diese Eigenschaft für ein Fenster festzulegen, verwenden Sie [**SHGetPropertyStoreForWindow,**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) um den Eigenschaftenspeicher des Fensters abzurufen, und verwenden Sie die Methoden von , die das [**IPropertyStore-Objekt**](/windows/win32/api/propsys/nn-propsys-ipropertystore) abgerufen haben, um die [System.AppUserModel.GineCommand-Eigenschaft]() dieses Fensters festzulegen.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchCommand
   shellPKey = PKEY_AppUserModel_RelaunchCommand
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a>Hinweise

PKEY-Werte werden in Propkey.h definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsbenutzermodell-IDs (AppUserModelIDs)](../shell/appids.md)
</dt> <dt>

[System.AppUserModel.ID](./props-system-appusermodel-id.md)
</dt> <dt>

[propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[aliasInfo](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[Stringformat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[Numberformat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[enum](./propdesc-schema-enum.md)
</dt> <dt>

[enumRange](./propdesc-schema-enumrange.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[Filtercontrol](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[relatedProperty](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
