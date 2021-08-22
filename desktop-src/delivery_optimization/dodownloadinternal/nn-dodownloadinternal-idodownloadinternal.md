---
title: IDODownloadInternal-Schnittstelle
description: Wird verwendet, um erweiterte Downloadeigenschaften abzurufen oder festzulegen.
keywords:
- IDODownloadInternal-Schnittstelle
topic_type:
- apiref
api_name:
- IDODownloadInternal
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: de9079f7b87822ce950bc4e6c3ece6457e62775c32f7c0d51e76959332298bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755780"
---
# <a name="idodownloadinternal-interface"></a>IDODownloadInternal-Schnittstelle

> [!IMPORTANT]
> Die **IDODownloadInternal-Schnittstelle** ist veraltet. Verwenden Sie stattdessen die [IDODownload-Schnittstelle.](../do/nn-do-idodownload.md)

Die **IDODownloadInternal-Schnittstelle** wird verwendet, um erweiterte Downloadeigenschaften abzurufen oder festzulegen.

## <a name="methods"></a>Methoden

Die **IDODownloadInternal-Schnittstelle** verfügt über diese Methoden.

| Methode | Beschreibung |
| ---- |:---- |
| [IDODownloadInternal::GetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | Ruft einen Zeiger auf eine **VARIANT-Datei** ab, die einen bestimmten erweiterten Downloadeigenschaftswert enthält. |
| [IDODownloadInternal::SetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | Legt eine erweiterte Downloadeigenschaft fest. Die -Methode akzeptiert  einen Zeiger auf eine VARIANT-Datei, die einen bestimmten Eigenschaftswert enthält, der auf den Download angewendet werden soll. |

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, nur Win32-Anwendungen der Version 1809 \[\] |
| **Header** | DODownloadInternal.h |