---
title: Idodownload-Schnittstelle
description: Wird verwendet, um einen Download zu starten und zu verwalten.
keywords:
- Idodownload-Schnittstelle
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
ms.openlocfilehash: ec2f74ce7daae6f612297d21e15e6993fcd78382
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315261"
---
# <a name="idodownload-interface"></a>Idodownload-Schnittstelle

Die **idodownload** -Schnittstelle wird verwendet, um einen Download zu starten und zu verwalten.

## <a name="methods"></a>Methoden

Die **idodownload** -Schnittstelle verfügt über diese Methoden.

| Methode | BESCHREIBUNG |
| ---- |:---- |
| [Idodownload:: Abort](./nf-do-idomanager-createdownload.md) | Bricht den Download ab. |
| [Idodownload:: Finalize](./nf-do-idodownload-finalize.md) | Schließt den Download ab. |
| [Idodownload:: GetProperty](./nf-do-idodownload-getproperty.md) | Ruft einen Zeiger auf eine **Variante** ab, die eine bestimmte Download Eigenschaft enthält. |
| [Idodownload:: GetStatus](./nf-do-idodownload-getstatus.md) | Ruft einen Zeiger auf eine **DO_DOWNLOAD_STATUS** -Struktur ab, die den aktuellen Status des Downloads widerspiegelt. |
| [Idodownload::P ause](./nf-do-idodownload-pause.md) | Hält den Download an. |
| [Idodownload:: SetProperty](./nf-do-idodownload-setproperty.md) | Legt eine Download Eigenschaft fest. |
| [Idodownload:: Start](./nf-do-idodownload-start.md) | Startet einen Download oder nimmt diesen wieder auf. |

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Do. h |