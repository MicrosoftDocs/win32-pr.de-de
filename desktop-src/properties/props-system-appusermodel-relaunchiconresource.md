---
description: Gibt das Symbol an, das für die Verknüpfung verwendet wird, die auf der Taskleiste erstellt wird, wenn der Benutzer eine Anwendung an die Taskleiste anheftet oder eine neue Instanz über die Sprungliste der Schaltfläche startet.
ms.assetid: 3559d1f5-988c-41d9-ba9a-dfa4ba643ee2
title: System.AppUserModel.IconResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b43394bd5ee7dca6084526224dac268500f6881317215d63d6fc0e9a126c5b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970839"
---
# <a name="systemappusermodelrelaunchiconresource"></a>System.AppUserModel.IconResource

Gibt das Symbol an, das für die Verknüpfung verwendet wird, die auf der Taskleiste erstellt wird, wenn der Benutzer eine Anwendung an die Taskleiste anheftet oder eine neue Instanz über die Sprungliste der Schaltfläche startet. Dies ist das Symbol, das für die Taskleistengruppe verwendet wird und für eine angeheftete Anwendung angezeigt wird, unabhängig davon, ob diese Anwendung ausgeführt wird oder nicht. Dies sollte in einem der folgenden Formate angegeben werden:

-   Standardressourcenformat, z.B. "%systemdir% \\ system32 \\shell32.dll,-128". Das Zeichen "-", bevor die Ressourcen-ID erforderlich ist. Verwenden Sie nicht das @-Zeichen am Anfang der Pfadzeichenfolge.
-   Direkter Pfad zu einer Symboldatei, z.B. "%programfiles% \\ Microsoft \\ Editor \\ Editor.ico,0". Beachten Sie, dass eine Ressourcen-ID in der Zeichenfolge erforderlich ist, da ICO-Dateien mehrere Symbolressourcen enthalten können. Wenn die ICO-Datei ein einzelnes Image ist, verwenden Sie "0" (ohne das Zeichen "-") als Ressourcen-ID.

[System.AppUserModel.IconResource]() ist eine optionale Eigenschaft. Wenn sie nicht festgelegt ist, wird das Symbol des Ziels des Befehls "neustart"[(System.AppUserModel.CsvCommand)](./props-system-appusermodel-relaunchcommand.md)verwendet. Da dies jedoch zu unerwünschten Ergebnissen führen kann, wird dringend empfohlen, über diese Eigenschaft explizit ein Symbol bereitzustellen.

Diese Eigenschaft wird nur verwendet, wenn ein Fenster über eine explizite Anwendungsbenutzermodell-ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), festgelegt über [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)) verfügt. Wenn das Fenster über keine explizite AppUserModelID (System.AppUserModel.ID) verfügt, wird diese Eigenschaft ignoriert, und das Fenster wird gruppiert und angeheftet, als wäre es Teil des besitzenden Prozesses. Weitere Informationen zur Anwendung expliziter AppUserModelIDs und deren Auswirkungen auf das Anheften auf die Taskleiste finden Sie unter [Anwendungsbenutzermodell-IDs (AppUserModelIDs).](../shell/appids.md) Diese Eigenschaft soll von Anwendungen oder Fenstern verwendet werden, die nicht standardmäßige Neustartinformationen bereitstellen möchten. Weitere Informationen finden Sie unter [System.AppUserModel.CsvCommand](./props-system-appusermodel-relaunchcommand.md).

Wenn eine explizite AppUserModelID im Fenster festgelegt ist, diese Eigenschaft jedoch nicht festgelegt ist, versucht das System, eine Verknüpfung mit derselben AppUserModelID zu finden, und heftet diese Verknüpfung an die Taskleiste an, um das Fenster darzustellen. Wenn keine solche Verknüpfung gefunden werden kann, wird die zugrunde liegende ausführbare Datei des Prozesses verwendet, der sie besitzt.

> [!Note]  
> Diese Eigenschaft wird ignoriert, wenn [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) festgelegt ist. Dadurch kann eine Anwendung die Gruppierung ihrer Fenster steuern, indem sie ihnen explizite AppUserModelIDs zuweist, aber verhindert, dass diese Fenster angeheftet werden.

 

Um diese Eigenschaft für ein Fenster festzulegen, verwenden Sie [**SHGetPropertyStoreForWindow,**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) um den Eigenschaftenspeicher des Fensters abzurufen, und verwenden Sie die Methoden von , die das [**IPropertyStore-Objekt**](/windows/win32/api/propsys/nn-propsys-ipropertystore) abgerufen haben, um die [System.AppUserModel.IconResource-Eigenschaft]() dieses Fensters festzulegen.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = false
```

## <a name="windows-8-windows-7"></a>Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

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

 

 
