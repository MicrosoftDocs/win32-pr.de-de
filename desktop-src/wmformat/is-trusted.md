---
title: Is_Trusted
description: Das Attribut Is Trusted ist ein Attribut auf Dateiebene, das an gibt, ob die \_ Lizenzerwerbs-URL in der Datei vertrauenswürdig ist.
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Is_Trusted des Windows-Medienformats
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e255c91c5779eb44da8e587601fdfd9264f10888a46a7f216ae2af619ff9f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118198276"
---
# <a name="is_trusted"></a>Ist \_ vertrauenswürdig

Das **Attribut Is \_ Trusted** ist ein Attribut auf Dateiebene, das an gibt, ob die Lizenzerwerbs-URL in der Datei vertrauenswürdig ist.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMTrusted

## <a name="data-type"></a>Datentyp

**\_WMT-TYP \_ BOOL**

## <a name="remarks"></a>Hinweise

Dies ist ein codiertes Attribut.

Vor dem Navigieren zu einer Lizenzerwerbs-URL, die in einer DRM-geschützten Datei enthalten ist, sollte eine Anwendung zunächst überprüfen, ob diese Eigenschaft true ist. Wenn der Wert FALSE ist, sollte die Anwendung den Benutzer benachrichtigen, dass die URL möglicherweise manipuliert wurde.

Dieses Attribut kann nicht auf Dateiebene dupliziert werden. Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und vermittelt den Objekten des Windows Media Format SDK nicht seine normale Bedeutung.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




