---
title: TaskSettings.NetworkSettings(Eigenschaft)
description: Für die Skripterstellung ruft das Netzwerkeinstellungsobjekt ab, das einen Netzwerkprofilbezeichner und -namen enthält, oder legt dieses fest.
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- NetworkSettings-Taskplaner
- NetworkSettings-Eigenschaft Taskplaner , TaskSettings-Objekt
- TaskSettings-Objekt Taskplaner , NetworkSettings-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 730701c71a69f05b73524d6f9d1d8ad3d89b5e93620664be33a80c5c41af1479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059657"
---
# <a name="tasksettingsnetworksettings-property"></a>TaskSettings.NetworkSettings(Eigenschaft)

Für die Skripterstellung ruft das Netzwerkeinstellungsobjekt ab, das einen Netzwerkprofilbezeichner und -namen enthält, oder legt dieses fest. Wenn die [**RunOnlyIfNetworkAvailable-Eigenschaft**](tasksettings-runonlyifnetworkavailable.md) von [**TaskSettings**](tasksettings.md) **true** ist und eine Netzwerkpropfile in der **NetworkSettings-Eigenschaft** angegeben ist, wird der Task nur ausgeführt, wenn das angegebene Netzwerkprofil verfügbar ist.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**NetworkSettings-Objekt,**](networksettings.md) das einen Netzwerkprofilbezeichner und -namen enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> </dl>

 

 





