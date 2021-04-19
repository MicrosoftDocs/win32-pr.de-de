---
description: Gibt das Symbol an, das für die Verknüpfung verwendet wird, die auf der Taskleiste erstellt wird, wenn der Benutzer eine Anwendung an die Taskleiste anheften oder über die Sprung Liste der Schaltfläche eine neue Instanz starten soll.
ms.assetid: 3559d1f5-988c-41d9-ba9a-dfa4ba643ee2
title: System. appusermodel. relaunchienresource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc79c246fef7be5641c6488dcc34169cd5bbf98b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355622"
---
# <a name="systemappusermodelrelaunchiconresource"></a>System. appusermodel. relaunchienresource

Gibt das Symbol an, das für die Verknüpfung verwendet wird, die auf der Taskleiste erstellt wird, wenn der Benutzer eine Anwendung an die Taskleiste anheften oder über die Sprung Liste der Schaltfläche eine neue Instanz starten soll. Dies ist das Symbol, das für die Task leisten Gruppe verwendet wird, und wird für eine fixierte Anwendung angezeigt, unabhängig davon, ob die Anwendung ausgeführt wird oder nicht. Dies sollte in einem der folgenden Formate angegeben werden:

-   Standard Ressourcen Format, z. b. "% systemdir% \\ system32 \\shell32.dll,-128". Das Zeichen "-" vor der Ressourcen-ID ist erforderlich. Verwenden Sie das Zeichen ' @ ' nicht an der Vorderseite der Pfad Zeichenfolge.
-   Direkter Pfad zu einer Symbol Datei, z. b. "% Program Files% \\ Microsoft \\ Notepad \\ . ico, 0". Beachten Sie, dass in der Zeichenfolge eine Ressourcen-ID erforderlich ist, da ICO-Dateien mehrere Symbol Ressourcen enthalten können. Wenn es sich bei der ICO-Datei um ein einzelnes Bild handelt, verwenden Sie "0" (ohne das Zeichen "-") als Ressourcen-ID.

[System. appusermodel. relaunchiesresource]() ist eine optionale Eigenschaft. Wenn Sie nicht festgelegt ist, wird das Symbol für das Ziel des Befehls "Relaunch" ([System. appusermodel. relaunchcommand](./props-system-appusermodel-relaunchcommand.md)) verwendet. Da dies jedoch zu unerwünschten Ergebnissen führen kann, empfehlen wir dringend, dass Sie ein Symbol explizit über diese Eigenschaft bereitstellen.

Diese Eigenschaft wird nur verwendet, wenn ein Fenster über eine explizite Anwendungs Benutzer Modell-ID (appusermodelid) verfügt ([System.AppUserModel.ID](./props-system-appusermodel-id.md), festgelegt über [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Wenn das Fenster nicht über eine explizite appusermodelid (System.AppUserModel.ID) verfügt, wird diese Eigenschaft ignoriert, und das Fenster wird so gruppiert und fixiert, als wäre es Teil des besitzenden Prozesses. Weitere Informationen zur Anwendung von expliziten appusermudelids und deren Auswirkungen auf das Anheften der Taskleiste finden Sie unter [Anwendungs Benutzer Modell-IDs (appusermudelids)](../shell/appids.md). Diese Eigenschaft soll von Anwendungen oder Fenstern verwendet werden, die nicht standardmäßige Neustarts-Informationen bereitstellen möchten. Weitere Informationen finden Sie unter [System. appusermodel. relaunchcommand](./props-system-appusermodel-relaunchcommand.md).

Wenn für das Fenster eine explizite appusermodelid festgelegt wird, diese Eigenschaft jedoch nicht festgelegt ist, versucht das System, eine Verknüpfung mit der gleichen appusermodelid zu finden, und heftet diese Verknüpfung mit der Taskleiste, um das Fenster darzustellen. Wenn keine solche Verknüpfung gefunden werden kann, wird die unterstützende ausführbare Datei des Prozesses verwendet, der Sie besitzt.

> [!Note]  
> Diese Eigenschaft wird ignoriert, wenn [System. appusermodel. preventpinning](./props-system-appusermodel-preventpinning.md) festgelegt ist. Dies ermöglicht es einer Anwendung, die Gruppierung ihrer Fenster zu steuern, indem Ihnen explizit appusermudelids zugewiesen wird, aber verhindert wird, dass diese Fenster fixiert werden.

 

Wenn Sie diese Eigenschaft für ein Fenster festlegen möchten, rufen Sie mithilfe von [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) den Eigenschaften Speicher des Fensters ab, und verwenden Sie die Methoden dieses abgerufenen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Objekts, um die [System. appusermodel. relaunchienresource]() -Eigenschaft dieses Fensters festzulegen.

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

 

 
