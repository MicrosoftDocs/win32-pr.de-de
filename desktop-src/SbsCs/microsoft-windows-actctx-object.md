---
description: The Microsoft. Windows. Das ActCtx-Objekt verweist auf Manifeste und bietet Skript-Engines die Möglichkeit, auf nebeneinander ausgeführte Assemblys zu zugreifen. The Microsoft. Windows. Das ActCtx-Objekt kann verwendet werden, um eine Instanz einer side-by-side-Assembly mit COM-Komponenten zu erstellen.
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: Microsoft. Windows. ActCtx-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Microsoft.Windows.ActCtx
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7e84eadbc7489ddd91c34c0c9494515e89205849829625e850ad31dce3e92fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142003"
---
# <a name="microsoftwindowsactctx-object"></a>Microsoft. Windows. ActCtx-Objekt

**Microsoft.Windows. Das ActCtx-Objekt** verweist auf Manifeste und bietet Skript-Engines die Möglichkeit, auf nebeneinander ausgeführte Assemblys zu zugreifen. **Microsoft.Windows. Das ActCtx-Objekt** kann verwendet werden, um eine Instanz einer side-by-side-Assembly mit COM-Komponenten zu erstellen.

**Microsoft.Windows. Das ActCtx-Objekt** wird als Assembly in Windows Server 2003 verwendet. Sie kann auch von Anwendungen installiert werden, die den Windows Installer für das Setup verwenden, und als Mergemodul in das Installationspaket ein schließen.

## <a name="members"></a>Member

**Microsoft.Windows. Das ActCtx-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

**Microsoft.Windows. Das ActCtx-Objekt** verfügt über diese Methoden.



| Methode                               | Beschreibung                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [**Createobject**](createobject.md) | Erstellt ein -Objekt im Kontext des aktuellen Manifests.<br/>            |
| [**Getobject**](getobject.md)       | Ruft eine Instanz einer vorhandenen **Microsoft.Windows. ActCtx-Objekt.**<br/> |



 

### <a name="properties"></a>Eigenschaften

**Microsoft.Windows. Das ActCtx-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                | Zugriffstyp          | Beschreibung                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [**Manifest**](manifest.md)<br/> | Schreibgeschützt<br/> | Ruft den aktiven Aktivierungskontext ab.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



 

 




