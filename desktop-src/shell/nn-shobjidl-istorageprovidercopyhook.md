---
description: Definiert eine Methode, die bestimmt, ob die Shell einen Ordner im Synchronisierungs Stamm eines cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.
title: IStorageProviderCopyHook-Schnittstelle
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: 52f2a7fb7c8d7b37fc27fd1e91c93d716bc92086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391784"
---
# <a name="istorageprovidercopyhook-interface"></a>IStorageProviderCopyHook-Schnittstelle

Macht eine Methode verfügbar, die bestimmt, ob die Shell einen Ordner im Synchronisierungs Stamm eines cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.

## <a name="members"></a>Member

Die **istorageprovidercopyhook** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Istorageprovidercopyhook** verfügt auch über die folgenden Typen von Membern:

- [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **istorageprovidercopyhook** -Schnittstelle verfügt über diese Methoden.



| Methode                                           | BESCHREIBUNG                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Copycallback**](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  Bestimmt, ob die Shell einen Ordner im Synchronisierungs Stamm eines cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.                                                           |


## <a name="requirements"></a>Requirements (Anforderungen)

| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 Insider Preview-Build 19624                                                |
| Header<br/>                   | shobjidl. h   |
