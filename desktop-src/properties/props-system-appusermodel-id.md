---
description: Eine explizite Anwendungsbenutzermodell-ID (AppUserModelID), die zum Zuordnen von Prozessen, Dateien und Fenstern zu einer bestimmten Anwendung verwendet wird.
ms.assetid: 07858b3c-e601-40ec-a87a-d66612d5473a
title: System.AppUserModel.ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd60b64598a620221ec2b610b10cbc05002f38aaf633e51e788b24797620cab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033738"
---
# <a name="systemappusermodelid"></a>System.AppUserModel.ID

Eine explizite Anwendungsbenutzermodell-ID (AppUserModelID), die zum Zuordnen von Prozessen, Dateien und Fenstern zu einer bestimmten Anwendung verwendet wird. In einigen Fällen ist es ausreichend, sich auf die interne AppUserModelID zu verlassen, die einem Prozess vom System zugewiesen wird. Eine Anwendung, die mehrere Prozesse besitzt, oder eine Anwendung, die in einem Hostprozess ausgeführt wird, muss sich jedoch möglicherweise explizit über diese Eigenschaft identifizieren, damit sie ihre ansonsten unterschiedlichen Fenster unter einer einzigen Taskleistenschaltfläche gruppieren und den Inhalt der Sprungliste dieser Anwendung steuern kann.

Um diese Eigenschaft für ein Fenster festzulegen, verwenden Sie [**SHGetPropertyStoreForWindow,**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) um den Eigenschaftenspeicher des Fensters abzurufen, und verwenden Sie die Methoden des abgerufenen [**IPropertyStore-Objekts,**](/windows/win32/api/propsys/nn-propsys-ipropertystore) um die [System.AppUserModel.ID]() Eigenschaft dieses Fensters festzulegen.

Weitere Informationen finden Sie unter [Anwendungsbenutzermodell-IDs (AppUserModelIDs).](../shell/appids.md)

Zum Zeitpunkt der Festlegung der [System.AppUserModel.ID-Eigenschaft]() wird die Taskleiste benachrichtigt, ihre Informationen im Fenster oder der Verknüpfung zu aktualisieren, wenn AppUserModelID angegeben ist.

Andere Fenster- und Verknüpfungseigenschaften können in Verbindung mit einer expliziten AppUserModelID verwendet werden, um die Gruppierung und Anheftung, die einem Fenster zugeordnet ist, den Anzeigenamen und das Symbol, die dafür in der Taskleiste verwendet werden, und den Befehl zum Starten einer Anwendung, die an die Taskleiste angeheftet ist, oder eine neue Instanz der Anwendung über die Sprungliste dieser Anwendung zu steuern. Diese Eigenschaften sollten vor dem Festlegen der [System.AppUserModel.ID]() -Eigenschaft festgelegt werden. Weitere Informationen finden Sie in den folgenden Themen:

-   [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md)
-   [System.AppUserModel.NeustartCommand](./props-system-appusermodel-relaunchcommand.md)
-   [System.AppUserModel.CsvDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [System.AppUserModel.IconResource](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.ID
   shellPKey = PKEY_AppUserModel_ID
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 5
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

[**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
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

 

 
