---
description: Eine explizite App-Benutzer Modell-ID (appusermodelid), die verwendet wird, um Prozesse, Dateien und Fenster einer bestimmten Anwendung zuzuordnen.
ms.assetid: 07858b3c-e601-40ec-a87a-d66612d5473a
title: System.AppUserModel.ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c636b2c946f1138f4a25c3129a7a3b44d31558
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344779"
---
# <a name="systemappusermodelid"></a>System.AppUserModel.ID

Eine explizite App-Benutzer Modell-ID (appusermodelid), die verwendet wird, um Prozesse, Dateien und Fenster einer bestimmten Anwendung zuzuordnen. In einigen Fällen ist es ausreichend, die interne appusermodelid zu verlassen, die einem Prozess vom System zugewiesen wird. Eine Anwendung, die mehrere Prozesse oder eine Anwendung besitzt, die in einem Host Prozess ausgeführt wird, muss sich jedoch möglicherweise explizit durch diese Eigenschaft identifizieren, damit Sie die ansonsten ungleichen Fenster unter einer einzigen Task leisten Schaltfläche gruppieren und den Inhalt der Sprung Liste der Anwendung steuern kann.

Wenn Sie diese Eigenschaft für ein Fenster festlegen möchten, rufen Sie mit [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) den Eigenschaften Speicher des Fensters ab, und verwenden Sie die Methoden dieses abgerufenen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Objekts, um die [System.AppUserModel.ID]() -Eigenschaft dieses Fensters festzulegen.

Weitere Informationen finden Sie unter [App-Benutzer Modell-IDs (appusermudelids)](../shell/appids.md).

Zu dem Zeitpunkt, an dem die [System.AppUserModel.ID]() -Eigenschaft festgelegt ist, wird die Taskleiste benachrichtigt, um die zugehörigen Informationen im Fenster oder in der Verknüpfung mit der entsprechenden appusermodelid zu aktualisieren.

Andere Fenster-und Verknüpfungs Eigenschaften können in Verbindung mit einer expliziten appusermodelid verwendet werden, um das Gruppieren und fixieren, das einem Fenster zugeordnet ist, den anzeigen Amen und das Symbol, das in der Taskleiste verwendet wird, und den Befehl zum Starten einer Anwendung, die an die Taskleiste angeheftet ist, bzw Diese Eigenschaften sollten vor dem Festlegen der [System.AppUserModel.ID]() -Eigenschaft festgelegt werden. Weitere Informationen finden Sie unter den folgenden Themen:

-   [System. appusermodel. preventpinning](./props-system-appusermodel-preventpinning.md)
-   [System. appusermodel. relaunchcommand](./props-system-appusermodel-relaunchcommand.md)
-   [System. appusermodel. relaunchdisplaynameresource](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [System. appusermodel. relaunchienresource](./props-system-appusermodel-relaunchiconresource.md)

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

## <a name="remarks"></a>Bemerkungen

Pkey-Werte werden in "propkey. h" definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Benutzer Modell-IDs (appusermudelids)](../shell/appids.md)
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

 

 
