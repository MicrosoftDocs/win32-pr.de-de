---
description: Gibt den anzeigen Amen an, der für die Verknüpfung verwendet wird, die auf der Taskleiste erstellt wird, wenn der Benutzer eine Anwendung an die Taskleiste anheften oder über die Sprung Liste der Schaltfläche eine neue Instanz starten soll.
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: System. appusermodel. relaunchdisplaynameresource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79c22d0ccecb8bac86fe5ca3636ed10ed2ca50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216098"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a>System. appusermodel. relaunchdisplaynameresource

Gibt den anzeigen Amen an, der für die Verknüpfung verwendet wird, die auf der Taskleiste erstellt wird, wenn der Benutzer eine Anwendung an die Taskleiste anheften oder über die Sprung Liste der Schaltfläche eine neue Instanz starten soll. Der Wert dieser Eigenschaft muss einer der folgenden sein:

-   Eine indirekte Ressourcen Zeichenfolge, z. b. "@% systemdir% \\ system32 \\shell32.dll,-19263". Beachten Sie, dass das Zeichen "@" erforderlich ist, um eine indirekte Zeichenfolge von einer nur-Text-Zeichenfolge zu unterscheiden (im nächsten aufzurufenen Absatz beschrieben). Diese indirekte Zeichenfolge besteht aus einer Binärdatei und einer Ressourcen-ID der Zeichenfolge, die in dieser Binärdatei enthalten ist. Es wird dringend empfohlen, dieses indirekte Zeichen folgen Formular zu verwenden, das sicherstellt, dass sich der Anzeige Name entsprechend ändert, wenn die Systemsprache über die mehrsprachige Benutzeroberfläche (MUI) geändert wird. Das Zeichen "-" vor der Ressourcen-ID ist erforderlich.
-   Eine klar Text Zeichenfolge, die nicht auf eine Ressource verweist. Dies sollte nur verwendet werden, wenn der Anzeige Name dynamisch berechnet oder aus einer Datenquelle abgerufen wird, die MUI nicht unterstützt. Die Zeichenfolge könnte z. b. der Name eines Geräts sein, z. b. "Microsoft Zune", in Fällen, in denen die Anwendung angezeigt wird, wenn das Gerät mit dem Computer verbunden ist.

> [!Note]  
> [System. appusermodel. relaunchcommand](./props-system-appusermodel-relaunchcommand.md) und [System. appusermodel. relaunchdisplaynameresource]() müssen immer zusammengesetzt werden. Wenn eine dieser Eigenschaften nicht festgelegt ist, wird keines von beiden verwendet.

 

Diese Eigenschaft wird nur verwendet, wenn ein Fenster über eine explizite Anwendungs Benutzer Modell-ID (appusermodelid) verfügt ([System.AppUserModel.ID](./props-system-appusermodel-id.md), festgelegt über [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Wenn das Fenster nicht über eine explizite appusermodelid verfügt, wird diese Eigenschaft ignoriert, und das Fenster wird gruppiert und angeheftet, als wäre es Teil des Prozesses, in dem es enthalten ist. Weitere Informationen zur Anwendung von expliziten appusermudelids und deren Auswirkungen auf das Anheften der Taskleiste finden Sie unter [Anwendungs Benutzer Modell-IDs (appusermudelids)](../shell/appids.md). Diese Eigenschaft soll von Anwendungen oder Fenstern verwendet werden, die nicht standardmäßige Neustarts-Informationen bereitstellen möchten. Weitere Informationen finden Sie unter [System. appusermodel. relaunchcommand](./props-system-appusermodel-relaunchcommand.md).

> [!Note]  
> Diese Eigenschaft wird ignoriert, wenn [System. appusermodel. preventpinning](./props-system-appusermodel-preventpinning.md) festgelegt ist. Dies ermöglicht es einer Anwendung, die Gruppierung ihrer Fenster zu steuern, indem Ihnen explizit appusermudelids zugewiesen wird, aber verhindert wird, dass diese Fenster fixiert werden.

 

Wenn Sie diese Eigenschaft für ein Fenster festlegen möchten, rufen Sie mit [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) den Eigenschaften Speicher des Fensters ab, und verwenden Sie die Methoden dieses abgerufenen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Objekts, um die [System. appusermodel. relaunchdisplaynameresource]() -Eigenschaft dieses Fensters festzulegen.

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

 

 
