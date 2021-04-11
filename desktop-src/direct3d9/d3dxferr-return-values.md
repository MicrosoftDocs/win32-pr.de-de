---
description: Die Methoden, die für die Arbeit mit DirectX. x-Dateien verwendet werden, können zusätzlich zu den Standard-com-Rückgabe Werten die folgenden Werte zurückgeben.
ms.assetid: b1d04fab-25cb-431d-942e-74092bc9c5c2
title: D3DXFERR-Rückgabewerte (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFERR
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: cab1cc5e70b6204c832fd9fe5b0fecac4276f578
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132344"
---
# <a name="d3dxferr-return-values"></a>D3DXFERR-Rückgabewerte

Die Methoden, die für die Arbeit mit DirectX. x-Dateien verwendet werden, können zusätzlich zu den Standard-com-Rückgabe Werten die folgenden Werte zurückgeben.

<dl> <dt>

<span id="D3DXFERR_BADARRAYSIZE"></span><span id="d3dxferr_badarraysize"></span>**D3DXFERR \_ badarraysize**
</dt> <dd>

Ein Array überschreitet die zulässige Größe.

</dd> <dt>

<span id="D3DXFERR_BADCACHEFILE"></span><span id="d3dxferr_badcachefile"></span>**D3DXFERR \_ badcachefile**
</dt> <dd>

Eine Cachedatei konnte nicht gelesen werden.

</dd> <dt>

<span id="D3DXFERR_BADDataReference"></span><span id="d3dxferr_baddatareference"></span><span id="D3DXFERR_BADDATAREFERENCE"></span>**D3DXFERR \_ baddatareferenzierung**
</dt> <dd>

Die Vorlagen Elementdaten konnten nicht abgerufen werden.

</dd> <dt>

<span id="D3DXFERR_BADFILE"></span><span id="d3dxferr_badfile"></span>**D3DXFERR \_ BadFile**
</dt> <dd>

Fehler beim Lesen oder Schreiben einer Datei.

</dd> <dt>

<span id="D3DXFERR_BADFILEFLOATSIZE"></span><span id="d3dxferr_badfilefloatsize"></span>**D3DXFERR \_ badfilefloatsize**
</dt> <dd>

Die Datei weist nicht die erwartete Größe auf.

</dd> <dt>

<span id="D3DXFERR_BADFILETYPE"></span><span id="d3dxferr_badfiletype"></span>**D3DXFERR \_ badfiletype**
</dt> <dd>

Die Datei weist ein ungültiges Format auf.

</dd> <dt>

<span id="D3DXFERR_BADFILEVERSION"></span><span id="d3dxferr_badfileversion"></span>**D3DXFERR \_ badfileversion**
</dt> <dd>

Die Format Version der Datei ist ungültig.

</dd> <dt>

<span id="D3DXFERR_BADOBJECT"></span><span id="d3dxferr_badobject"></span>**D3DXFERR \_ badobject**
</dt> <dd>

Daten konnten nicht aus einem Objekt gelesen oder geschrieben werden.

</dd> <dt>

<span id="D3DXFERR_BADRESOURCE"></span><span id="d3dxferr_badresource"></span>**D3DXFERR \_ badresource**
</dt> <dd>

Ein Vorgang für eine Ressource ist fehlgeschlagen.

</dd> <dt>

<span id="D3DXFERR_BADTYPE"></span><span id="d3dxferr_badtype"></span>**D3DXFERR \_ badtype**
</dt> <dd>

Die Datei entsprach nicht den bekannten Vorlagen Typen.

</dd> <dt>

<span id="D3DXFERR_BADVALUE"></span><span id="d3dxferr_badvalue"></span>**D3DXFERR \_ badvalue**
</dt> <dd>

Eine Variable liegt außerhalb des erwarteten Bereichs. wird in der Regel zurückgegeben, wenn ein Objekt Zeiger ungültig ist.

</dd> <dt>

<span id="D3DXFERR_FILENOTFOUND"></span><span id="d3dxferr_filenotfound"></span>**D3DXFERR file \_ Topics**
</dt> <dd>

Für die angegebene Datei konnte kein gültiger Handle gefunden werden.

</dd> <dt>

<span id="D3DXFERR_NOMOREDATA"></span><span id="d3dxferr_nomoredata"></span>**D3DXFERR \_ nomoredata**
</dt> <dd>

Der Zeiger Offset wurde über das Ende des Puffers hinaus erweitert.

</dd> <dt>

<span id="D3DXFERR_NOMOREOBJECTS"></span><span id="d3dxferr_nomoreobjects"></span>**D3DXFERR \_ nomoreobjects**
</dt> <dd>

Es sind keine weiteren untergeordneten Objekte verfügbar.

</dd> <dt>

<span id="D3DXFERR_NOTDONEYET"></span><span id="d3dxferr_notdoneyet"></span>**D3DXFERR \_ notdoneyet**
</dt> <dd>

Der Datentyp entsprach nicht den zulässigen Typen.

</dd> <dt>

<span id="D3DXFERR_NOTFOUND"></span><span id="d3dxferr_notfound"></span>**D3DXFERR \_ NotFound**
</dt> <dd>

Das Objekt konnte aus den angegebenen Parametern nicht gefunden werden.

</dd> <dt>

<span id="D3DXFERR_PARSEERROR"></span><span id="d3dxferr_parseerror"></span>**D3DXFERR- \_ Analysefehler**
</dt> <dd>

Der Datenstream konnte nicht analysiert werden.

</dd> <dt>

<span id="D3DXFERR_RESOURCENOTFOUND"></span><span id="d3dxferr_resourcenotfound"></span>**D3DXFERR \_ resourcenotfound**
</dt> <dd>

Für die angegebene Ressource konnte kein gültiges Handle gefunden werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Datei Fehler-Code der Datei ". x" \_ FACD3DXF wird verwendet, um Fehlercodes zu generieren. Beispiel:


```
#define _FACD3DXF           0x876
#define D3DXFERR_BADOBJECT  MAKE_HRESULT( 1, _FACD3DXF, 900 )
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX X-Datei Konstanten](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> </dl>

 

 




