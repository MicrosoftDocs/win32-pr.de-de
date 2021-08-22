---
title: WM/ContainerFormat
description: Das WM/ContainerFormat-Attribut gibt den Dateityp an, der in das aufrufende Objekt geladen wird.
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- WM/ContainerFormat windows Media Format
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e0d5cc430b0580c6719d212d664d8c19ddc65eee64e5877a8e6aba80d94a6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839440"
---
# <a name="wmcontainerformat"></a>WM/ContainerFormat

Das **WM/ContainerFormat-Attribut** gibt den Dateityp an, der in das aufrufende Objekt geladen wird.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMContainerFormat

## <a name="data-type"></a>Datentyp

[**WMT \_ \_SPEICHERFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**\_ WMT-TYP \_ BINARY**)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird anstelle von **IWMProfile3::GetStorageFormat** und **IWMProfile3::SetStorageFormat** verwendet, die nicht mehr unterstützt werden.

Dies ist ein codiertes Attribut.

Dieses Attribut kann nicht auf Dateiebene dupliziert werden. Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und vermittelt den Objekten des Windows Media Format SDK nicht seine normale Bedeutung.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




