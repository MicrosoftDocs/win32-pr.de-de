---
title: Idodownloadinternal-Schnittstelle
description: Wird verwendet, um Erweiterte Download Eigenschaften zu erhalten oder festzulegen.
keywords:
- Idodownloadinternal-Schnittstelle
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
ms.openlocfilehash: 89dcf0e397e9761c1b156a4ad4b245209cf50020
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102015"
---
# <a name="idodownloadinternal-interface"></a>Idodownloadinternal-Schnittstelle

> [!IMPORTANT]
> Die **idodownloadinternal** -Schnittstelle ist veraltet. Verwenden Sie stattdessen die [idodownload](../do/nn-do-idodownload.md) -Schnittstelle.

Die **idodownloadinternal** -Schnittstelle wird verwendet, um Erweiterte Download Eigenschaften zu erhalten oder festzulegen.

## <a name="methods"></a>Methoden

Die **idodownloadinternal** -Schnittstelle verfügt über diese Methoden.

| Methode | BESCHREIBUNG |
| ---- |:---- |
| [Idodownloadinternal:: getpropertyex](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | Ruft einen Zeiger auf einen **Variant** -Wert ab, der einen bestimmten erweiterten Download-Eigenschafts Wert enthält. |
| [Idodownloadinternal:: setpropertyex](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | Legt eine erweiterte Download Eigenschaft fest. Die-Methode akzeptiert einen Zeiger auf eine **Variante** , die einen bestimmten Eigenschafts Wert enthält, der auf den Download angewendet werden soll. |

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Dodownloadinternal. h |