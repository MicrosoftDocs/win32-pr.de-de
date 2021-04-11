---
description: Gibt an, ob die Anwendung die Microsoft Direct3D-Unterstützung im Quell-oder senkenwriter erfordert.
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: MF_READWRITE_D3D_OPTIONAL-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8c78295dd12e5d187c9be380305dc225d7e8e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218239"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a>MF, \_ Lese schreiben \_ D3D \_ optionales Attribut

Gibt an, ob die Anwendung die Microsoft Direct3D-Unterstützung im [Quell](source-reader.md) -oder [senkenwriter](sink-writer.md)erfordert.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt nur, wenn die Anwendung die Direct3D-Unterstützung mithilfe des [MF- \_ Quell \_ Readers \_ D3D \_ Manager](mf-source-reader-d3d-manager.md) -oder [MF \_ Sink \_ Writer \_ D3D \_ Manager](mf-sink-writer-d3d-manager.md) -Attributs ermöglicht.

Wenn die Anwendung die Direct3D-Unterstützung aktiviert, versuchen sowohl der Quell-als auch der senkwriter, Direct3D-Oberflächen für Videos zuzuordnen. Wenn dies nicht der Fall ist und das Attribut "read Read D3D optional" den Wert " \_ \_ \_ **true**" hat, wird der quelllese-/senkwriter auf die Zuordnung von Video Oberflächen im Systemspeicher zurückgegriffen. Andernfalls tritt bei der Verarbeitung ein Fehler auf, wenn Direct3D-Oberflächen nicht zugeordnet werden können und der MF- \_ Lesevorgang \_ D3D \_ optional **false** ist.

Wenn die Anwendung die Direct3D-Unterstützung nicht aktiviert, verwendet der Quell-/senuswriter System Arbeitsspeicher und ignoriert den Wert von MF- \_ lesenschreib \_ D3D \_ optional.

Dieses Attribut ist optional. Der Standardwert ist **FALSE**. Legen Sie das-Attribut fest, wenn Sie den Quell-oder Senke-Writer erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>"Mfreadwrite. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Senkenwriter-Attribute](sink-writer-attributes.md)
</dt> <dt>

[Attribute des Quell Readers](source-reader-attributes.md)
</dt> </dl>

 

 




