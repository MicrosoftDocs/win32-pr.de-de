---
description: Gibt den Anzeigenamen an, der für die Verknüpfung verwendet wird, die auf der Taskleiste erstellt wird, wenn der Benutzer eine Anwendung an die Taskleiste anheftet oder eine neue Instanz über die Sprungliste der Schaltfläche startet.
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: System.AppUserModel.CsvDisplayNameResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b0af752fb345dd5dd5f1b091a22255e856031affaca266ff6307045f148cd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233022"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a>System.AppUserModel.CsvDisplayNameResource

Gibt den Anzeigenamen an, der für die Verknüpfung verwendet wird, die auf der Taskleiste erstellt wird, wenn der Benutzer eine Anwendung an die Taskleiste anheftet oder eine neue Instanz über die Sprungliste der Schaltfläche startet. Der Wert dieser Eigenschaft muss einer der folgenden Sein:

-   Eine indirekte Ressourcenzeichenfolge wie "@%systemdir% \\ system32 \\shell32.dll,-19263". Beachten Sie, dass das @-Zeichen erforderlich ist, um eine indirekte Zeichenfolge von einer Nur-Text-Zeichenfolge zu unterscheiden (wie im nächsten Absatz mit Aufzählungszeichen beschrieben). Diese indirekte Zeichenfolge besteht aus einer Binärdatei und einer Ressourcen-ID der Zeichenfolge, die in dieser Binärdatei enthalten ist. Es wird dringend empfohlen, dieses indirekte Zeichenfolgenformular zu verwenden. Dadurch wird sichergestellt, dass sich der Anzeigename entsprechend ändert, wenn die Systemsprache über die mehrsprachige Benutzeroberfläche geändert wird. Das Zeichen "-", bevor die Ressourcen-ID erforderlich ist.
-   Eine Nur-Text-Zeichenfolge, die nicht auf eine Ressource verweist. Dies sollte nur verwendet werden, wenn der Anzeigename dynamisch berechnet oder aus einer Datenquelle abgerufen wird, die NOTE nicht unterstützt. Die Zeichenfolge kann beispielsweise der Name eines Geräts sein, z. B. "Microsoft Zune", wenn die Anwendung angezeigt wird, wenn das Gerät an den Computer angeschlossen ist.

> [!Note]  
> [System.AppUserModel.CsvCommand](./props-system-appusermodel-relaunchcommand.md) und [System.AppUserModel.NeustartDisplayNameResource]() müssen immer zusammen festgelegt werden. Wenn eine dieser Eigenschaften nicht festgelegt ist, wird keine dieser Eigenschaften verwendet.

 

Diese Eigenschaft wird nur verwendet, wenn ein Fenster über eine explizite Anwendungsbenutzermodell-ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), festgelegt über [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)) verfügt. Wenn das Fenster nicht über eine explizite AppUserModelID verfügt, wird diese Eigenschaft ignoriert, und das Fenster wird gruppiert und angeheftet, als wäre es Teil des Prozesses, der es besitzt. Weitere Informationen zur Anwendung expliziter AppUserModelIDs und deren Auswirkungen auf das Anheften auf die Taskleiste finden Sie unter [Anwendungsbenutzermodell-IDs (AppUserModelIDs).](../shell/appids.md) Diese Eigenschaft soll von Anwendungen oder Fenstern verwendet werden, die nicht standardmäßige Neustartinformationen bereitstellen möchten. Weitere Informationen finden Sie unter [System.AppUserModel.CsvCommand](./props-system-appusermodel-relaunchcommand.md).

> [!Note]  
> Diese Eigenschaft wird ignoriert, wenn [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) festgelegt ist. Dadurch kann eine Anwendung die Gruppierung ihrer Fenster steuern, indem sie ihnen explizite AppUserModelIDs zuweist, aber verhindert, dass diese Fenster angeheftet werden.

 

Um diese Eigenschaft in einem Fenster festzulegen, verwenden Sie [**SHGetPropertyStoreForWindow,**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) um den Eigenschaftenspeicher des Fensters abzurufen, und verwenden Sie die Methoden von , die das [**IPropertyStore-Objekt**](/windows/win32/api/propsys/nn-propsys-ipropertystore) abgerufen haben, um die [System.AppUserModel.GineDisplayNameResource-Eigenschaft]() dieses Fensters festzulegen.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchDisplayNameResource
   shellPKey = PKEY_AppUserModel_RelaunchDisplayNameResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 4
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

 

 
