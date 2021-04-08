---
title: WM/Containerformat
description: Das Attribut WM/Containerformat gibt den Dateityp an, der in das aufrufende Objekt geladen wird.
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- WM/Containerformat Windows Media-Format
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9394fca14c3e07eb1f867c7b8ac473b2b61a9a2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718593"
---
# <a name="wmcontainerformat"></a>WM/Containerformat

Das Attribut **WM/Containerformat** gibt den Dateityp an, der in das aufrufende Objekt geladen wird.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmcontainerformat

## <a name="data-type"></a>Datentyp

[**WMT \_ Speicher \_ Format**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**WMT \_ - \_ typbinär Datei**)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird anstelle von **IWMProfile3:: getstorageformat** und **IWMProfile3:: setstorageformat** verwendet, die nicht mehr unterstützt werden.

Dies ist ein codiertes Attribut.

Dieses Attribut kann nicht auf Dateiebene dupliziert werden. Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und gibt seine normale Bedeutung nicht an die Objekte des Windows Media Format SDK aus.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




