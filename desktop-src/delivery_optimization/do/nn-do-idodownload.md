---
title: IDODownload-Schnittstelle
description: Wird zum Starten und Verwalten eines Downloads verwendet.
keywords:
- IDODownload-Schnittstelle
topic_type:
- apiref
api_name:
- IDODownload
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 356d6ae2e01f91eae94d9d2ff01a39dd49708eb73a7287d8c176b4231654a74a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543817"
---
# <a name="idodownload-interface"></a>IDODownload-Schnittstelle

Die **IDODownload-Schnittstelle** wird verwendet, um einen Download zu starten und zu verwalten.

## <a name="methods"></a>Methoden

Die **IDODownload-Schnittstelle** verfügt über diese Methoden.

| Methode | BESCHREIBUNG |
| ---- |:---- |
| [IDODownload::Abort](./nf-do-idomanager-createdownload.md) | Bricht den Download ab. |
| [IDODownload::Finalize](./nf-do-idodownload-finalize.md) | Finalisiert den Download. |
| [IDODownload::GetProperty](./nf-do-idodownload-getproperty.md) | Ruft einen Zeiger auf eine **VARIANT-Datei** ab, die eine bestimmte Downloadeigenschaft enthält. |
| [IDODownload::GetStatus](./nf-do-idodownload-getstatus.md) | Ruft einen Zeiger auf eine **DO_DOWNLOAD_STATUS** Struktur ab, die den aktuellen Status des Downloads widerspiegelt. |
| [IDODownload::P ause](./nf-do-idodownload-pause.md) | Hält den Download an. |
| [IDODownload::SetProperty](./nf-do-idodownload-setproperty.md) | Legt eine Downloadeigenschaft fest. |
| [IDODownload::Start](./nf-do-idodownload-start.md) | Startet oder setzt einen Download fort. |

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, nur Win32-Anwendungen der Version 1809 \[\] |
| **Header** | Do.h |