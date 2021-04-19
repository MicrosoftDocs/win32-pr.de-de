---
description: Gibt einen Befehl an, der durch ShellExecute ausgeführt werden kann, um eine Anwendung zu starten, wenn Sie an die Taskleiste angeheftet ist, oder wenn eine neue Instanz der Anwendung über die Sprung Liste der Anwendung gestartet wird.
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: System. appusermodel. relaunchcommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84049f605896ba5e99a98f33557e6ee4dea37df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360176"
---
# <a name="systemappusermodelrelaunchcommand"></a>System. appusermodel. relaunchcommand

Gibt einen Befehl an, der durch [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) ausgeführt werden kann, um eine Anwendung zu starten, wenn Sie an die Taskleiste angeheftet ist, oder wenn eine neue Instanz der Anwendung über die Sprung Liste der Anwendung gestartet wird.

Einige Beispiele dafür sind:


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



Diese Eigenschaft wird nur verwendet, wenn ein Fenster über eine explizite Anwendungs Benutzer Modell-ID (appusermodelid) verfügt ([System.AppUserModel.ID](./props-system-appusermodel-id.md), festgelegt über [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Wenn das Fenster nicht über eine explizite appusermodelid verfügt, wird diese Eigenschaft ignoriert, und das Fenster wird gruppiert und angeheftet, als wäre es Teil des Prozesses, in dem es enthalten ist. Weitere Informationen zur Anwendung von expliziten appusermudelids und deren Auswirkungen auf das Anheften der Taskleiste finden Sie unter [Anwendungs Benutzer Modell-IDs (appusermudelids)](../shell/appids.md).

Diese Eigenschaft soll von Anwendungen oder Fenstern verwendet werden, die nicht standardmäßige Neustarts-Informationen bereitstellen möchten.

> [!Note]  
> [System. appusermodel. relaunchcommand]() und [System. appusermodel. relaunchdisplaynameresource](./props-system-appusermodel-relaunchdisplaynameresource.md) müssen immer zusammengesetzt werden. Wenn eine dieser Eigenschaften nicht festgelegt ist, wird keines von beiden verwendet.

 

Diese Eigenschaft kann zusammen mit " [System. appusermodel. relaunchdisplaynameresource](./props-system-appusermodel-relaunchdisplaynameresource.md) " und " [System. appusermodel. relaunchifiresource](./props-system-appusermodel-relaunchiconresource.md) " verwendet werden, um ein Fenster visuell als Anwendung für den Benutzer zu definieren. Dies ist nützlich für Host Anwendungsszenarien, in denen eine einzelne Host Instanz mehrere untergeordnete Anwendungen ausführt. Beispielsweise kann es vorkommen, dass ein virtueller Computer, auf dem mehrere virtualisierte Anwendungen gehostet werden, die virtualisierten Anwendungen als individuelle Anwendungen für den Benutzer angezeigt werden soll. Die virtuelle Maschine kann jedes Fenster mit einer expliziten appusermodelid und den entsprechenden Neustart Eigenschaften bezeichnen, damit Sie als Anwendungen angezeigt werden. Der Benutzer kann Sie dann an die Taskleiste anheften und die angeheftete Instanz "neu starten".

> [!Note]  
> Diese Eigenschaft wird ignoriert, wenn [System. appusermodel. preventpinning](./props-system-appusermodel-preventpinning.md) festgelegt ist. Dies ermöglicht es einer Anwendung, die Gruppierung ihrer Fenster zu steuern, indem Ihnen explizit appusermudelids zugewiesen wird, aber verhindert wird, dass diese Fenster fixiert werden.

 

Wenn Sie diese Eigenschaft für ein Fenster festlegen möchten, rufen Sie mithilfe von [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) den Eigenschaften Speicher des Fensters ab, und verwenden Sie die Methoden dieses abgerufenen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Objekts, um die [System. appusermodel. relaunchcommand]() -Eigenschaft dieses Fensters festzulegen.

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

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Benutzer Modell-IDs (appusermudelids)](../shell/appids.md)
</dt> <dt>

[System.AppUserModel.ID](./props-system-appusermodel-id.md)
</dt> <dt>

[propertydescriptionlist](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[propertydescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[SearchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[Labelinfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[TypeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[Display Info](./propdesc-schema-displayinfo.md)
</dt> <dt>

[aliasInfo](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[StringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[BooleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[NumberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedlist](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[enum](./propdesc-schema-enum.md)
</dt> <dt>

[enumbereich](./propdesc-schema-enumrange.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> <dt>

[DrawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editcontrol](./propdesc-schema-editcontrol.md)
</dt> <dt>

[FilterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[querycontrol](./propdesc-schema-querycontrol.md)
</dt> <dt>

[relatedpropertyinfo](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[relatedProperty](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
