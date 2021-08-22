---
title: IDOManager-Schnittstelle
description: Wird zum Erstellen eines neuen Downloads und zum Aufzählen vorhandener Downloads verwendet.
keywords:
- IDOManager-Schnittstelle
topic_type:
- apiref
api_name:
- IDOManager
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5fff72067c69345a9852718c377b179d16f398c0eb3b84c73ca82c3af1b08a71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047088"
---
# <a name="idomanager-interface"></a>IDOManager-Schnittstelle

Die **IDOManager-Schnittstelle** wird verwendet, um einen neuen Download zu erstellen und vorhandene Downloads aufzählen.

## <a name="methods"></a>Methoden

Die **IDOManager-Schnittstelle** verfügt über diese Methoden.

| Methode | Beschreibung |
| ---- |:---- |
| [IDOManager::CreateDownload](./nf-do-idomanager-createdownload.md) | Erstellt einen neuen Download. |
| [IDOManager::EnumDownloads](./nf-do-idomanager-enumdownloads.md) | Ruft einen Schnittstellenzeiger auf ein Enumeratorobjekt ab, das zum Aufzählen vorhandener Downloads verwendet wird. |

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, version 1809 Win32 applications only (Nur \[ Win32-Anwendungen der Version 1809)\] |
| **Header** | Do.h |