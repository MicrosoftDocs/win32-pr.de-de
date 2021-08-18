---
description: Definiert eine Methode, die bestimmt, ob die Shell einen Ordner im Synchronisierungsstamm eines Cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.
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
ms.openlocfilehash: aa26a329bd80295a6a46a1bb11d1dc651baf1ea71975576ed704b29a7fee8b57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968869"
---
# <a name="istorageprovidercopyhook-interface"></a>IStorageProviderCopyHook-Schnittstelle

Macht eine Methode verfügbar, die bestimmt, ob die Shell einen Ordner im Synchronisierungsstamm eines Cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.

## <a name="members"></a>Member

Die **IStorageProviderCopyHook-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IStorageProviderCopyHook** verfügt auch über diese Membertypen:

- [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IStorageProviderCopyHook-Schnittstelle** verfügt über diese Methoden.



| Methode                                           | BESCHREIBUNG                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**CopyCallback**](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  Bestimmt, ob die Shell einen Ordner im Synchronisierungsstamm eines Cloudanbieters verschieben, kopieren, löschen oder umbenennen darf.                                                           |


## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 Insider Preview Build 19624                                                |
| Header<br/>                   | shobjidl.h   |
