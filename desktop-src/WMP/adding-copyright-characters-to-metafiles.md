---
title: Hinzufügen von Copyrightzeichen zu Metadateien
description: Die Zeichen für Copyright- und Markenregistrierungssymbole ( \ 169; oder \ 174; ) werden möglicherweise nicht ordnungsgemäß angezeigt, wenn die Metadatei nicht mit dem UTF-8-Codierungsschema codiert ist.
ms.assetid: 9124c8d4-1fc1-4163-ada9-d96af58f8b98
keywords:
- Hinzufügen von Copyrightzeichen zu Metadateien Windows Media Player
topic_type:
- apiref
api_name:
- Adding Copyright Characters to Metafiles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b0ab5fc4e539331406bb776a4bcdacbed6578a234dd9e84a3c358cdbe9936ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865160"
---
# <a name="adding-copyright-characters-to-metafiles"></a>Hinzufügen von Copyrightzeichen zu Metadateien

Die Zeichen für Copyright- und Markenregistrierungssymbole ( © oder ® ) werden möglicherweise nicht ordnungsgemäß angezeigt, wenn die Metadatei nicht mit dem UTF-8-Codierungsschema codiert ist. In diesem Fall können Sie die ASCII-Entsprechungen (c) und (r) innerhalb des **COPYRIGHT-Elements** verwenden, um eines dieser Symbole für alle Benutzer ordnungsgemäß anzuzeigen, wie im folgenden Code gezeigt.


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



Wenn die Metadatei mit UTF-8 codiert wird, werden Copyright- und Markensymbole ordnungsgemäß angezeigt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




