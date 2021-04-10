---
description: Deaktiviert die Möglichkeit, eine Verknüpfung oder ein Fenster an die Taskleiste oder das Startmenü anzuheften. Diese Eigenschaft bewirkt außerdem, dass das Element in die Liste der am häufigsten verwendeten (MFU) Startmenüs aufgenommen wird.
ms.assetid: 86239BF8-BCFC-4e76-BF94-5ABA4639562C
title: System. appusermodel. preventpinning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804c615bcb35909610b06622bd25fe3dccdd0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865564"
---
# <a name="systemappusermodelpreventpinning"></a>System. appusermodel. preventpinning

Deaktiviert die Möglichkeit, eine Verknüpfung oder ein Fenster an die Taskleiste oder das **Startmenü** anzuheften. Diese Eigenschaft bewirkt außerdem, dass das Element in die Liste der am häufigsten verwendeten (MFU) **Startmenüs** aufgenommen wird.

Diese Eigenschaft muss in einem Fenster vor der Eigenschaft [pkey \_ appusermodel \_ ID](./props-system-appusermodel-id.md) festgelegt werden. Nachdem die pkey- \_ appusermodel- \_ ID-Eigenschaft festgelegt wurde, werden Änderungen an der [pkey- \_ appusermodel \_ ]() -Ausführung ignoriert.

Weitere Informationen zu App-Benutzer Modell-IDs (appusermudelids) und anderen Methoden zum Ausschließen eines Elements an die Taskleiste und zum Einbinden von MFU finden Sie unter [Anwendungs Benutzer Modell-IDs (appusermudelids)](../shell/appids.md).

Wenn Sie diese Eigenschaft für ein Fenster festlegen möchten, rufen Sie mit [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) den Eigenschaften Speicher des Fensters ab, und verwenden Sie die Methoden dieses abgerufenen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Objekts, um die [System. appusermodel. preventpinning]() -Eigenschaft dieses Fensters festzulegen.

Das Festlegen dieser Eigenschaft bewirkt, dass die folgenden Eigenschaften ignoriert werden:

-   [System. appusermodel. relaunchcommand](./props-system-appusermodel-relaunchcommand.md)
-   [System. appusermodel. relaunchdisplaynameresource](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [System. appusermodel. relaunchienresource](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.PreventPinning
   shellPKey = PKEY_AppUserModel_PreventPinning
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
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

[**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
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

 

 
