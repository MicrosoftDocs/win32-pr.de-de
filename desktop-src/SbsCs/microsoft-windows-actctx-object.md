---
description: Das Microsoft. Windows. ActCtx-Objekt verweist auf Manifeste und bietet eine Möglichkeit für Skript-Engines, auf parallele Assemblys zuzugreifen. Das Microsoft. Windows. ActCtx-Objekt kann verwendet werden, um eine Instanz einer parallelen Assembly mit COM-Komponenten zu erstellen.
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
ms.openlocfilehash: 58290ec9d36d8e8428000422d0e1014335870149
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864212"
---
# <a name="microsoftwindowsactctx-object"></a>Microsoft. Windows. ActCtx-Objekt

Das **Microsoft. Windows. ActCtx** -Objekt verweist auf Manifeste und bietet eine Möglichkeit für Skript-Engines, auf parallele Assemblys zuzugreifen. Das **Microsoft. Windows. ActCtx** -Objekt kann verwendet werden, um eine Instanz einer parallelen Assembly mit COM-Komponenten zu erstellen.

Das **Microsoft. Windows. ActCtx** -Objekt ist als Assembly in Windows Server 2003 verfügbar. Sie kann auch von Anwendungen installiert werden, die die Windows Installer für Setup verwenden, und Sie als Mergemodul in das Installationspaket einschließen.

## <a name="members"></a>Member

Das **Microsoft. Windows. ActCtx** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Microsoft. Windows. ActCtx** -Objekt verfügt über diese Methoden.



| Methode                               | BESCHREIBUNG                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [**CreateObject**](createobject.md) | Erstellt ein-Objekt im Kontext des aktuellen Manifests.<br/>            |
| [**GetObject**](getobject.md)       | Ruft eine Instanz eines vorhandenen **Microsoft. Windows. ActCtx** -Objekts ab.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **Microsoft. Windows. ActCtx** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                | Zugriffstyp          | BESCHREIBUNG                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [**Kundiger**](manifest.md)<br/> | Schreibgeschützt<br/> | Ruft den aktiven Aktivierungs Kontext ab.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



 

 




