---
description: Gibt an, ob die Anwendung Microsoft Direct3D-Unterstützung im Quelllese- oder Senkenwriter erfordert.
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: MF_READWRITE_D3D_OPTIONAL Attribut (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cebc24991e5c2bfb90b7153f3a90a2e7447c2daef987b2956680e89f162223ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664110"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a>MF \_ READWRITE \_ D3D \_ OPTIONAL-Attribut

Gibt an, ob die Anwendung Microsoft Direct3D-Unterstützung im [Quelllese-](source-reader.md) oder [Senkenwriter](sink-writer.md)benötigt.

## <a name="data-type"></a>Datentyp

**BOOL** als **UINT32** gespeichert

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt nur, wenn die Anwendung direct3D-Unterstützung mit dem [MF \_ SOURCE READER \_ \_ D3D \_ MANAGER-](mf-source-reader-d3d-manager.md) oder [MF SINK WRITER \_ \_ \_ D3D \_ MANAGER-Attribut](mf-sink-writer-d3d-manager.md) aktiviert.

Wenn die Anwendung direct3D-Unterstützung aktiviert, versuchen sowohl der Quellleser als auch der Sink Writer, Direct3D-Oberflächen für Videos zuzuordnen. Wenn dies fehlschlägt und das MF \_ READWRITE \_ D3D \_ OPTIONAL-Attribut **TRUE** ist, führt der Source Reader/Sink Writer einen Fallback auf die Zuweisung von Videooberflächen im Systemspeicher durch. Andernfalls tritt während der Verarbeitung ein Fehler auf, wenn Direct3D-Oberflächen nicht zugeordnet werden können und MF \_ READWRITE \_ D3D \_ OPTIONAL **FALSE** ist.

Wenn die Anwendung die Direct3D-Unterstützung nicht aktiviert, verwendet der Quelllese-/Senkenwriter Systemspeicher und ignoriert den Wert von MF \_ READWRITE \_ D3D \_ OPTIONAL.

Dieses Attribut ist optional. Der Standardwert ist **FALSE**. Legen Sie das Attribut fest, wenn Sie den Quelllese- oder Senkenwriter erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Sink Writer-Attribute](sink-writer-attributes.md)
</dt> <dt>

[Quellleseattribute](source-reader-attributes.md)
</dt> </dl>

 

 




