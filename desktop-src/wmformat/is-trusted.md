---
title: Is_Trusted
description: Das is \_ Trusted-Attribut ist ein Attribut auf Dateiebene, das angibt, ob die Lizenz Erwerbs-URL in der Datei vertrauenswürdig ist.
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Is_Trusted Windows Media-Format
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e8dd4fdd638bad0908bb1bbf50135cde5bad6c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948264"
---
# <a name="is_trusted"></a>Ist \_ vertrauenswürdig

Das **is \_ Trusted** -Attribut ist ein Attribut auf Dateiebene, das angibt, ob die Lizenz Erwerbs-URL in der Datei vertrauenswürdig ist.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmtrusted

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ bool**

## <a name="remarks"></a>Bemerkungen

Dies ist ein codiertes Attribut.

Bevor Sie zu einer Lizenz Erwerbs-URL navigieren, die in einer DRM-geschützten Datei enthalten ist, muss eine Anwendung zunächst überprüfen, ob diese Eigenschaft true ist. Wenn der Wert false ist, sollte die Anwendung den Benutzer benachrichtigen, dass die URL möglicherweise manipuliert wurde.

Dieses Attribut kann nicht auf Dateiebene dupliziert werden. Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und gibt seine normale Bedeutung nicht an die Objekte des Windows Media Format SDK aus.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




