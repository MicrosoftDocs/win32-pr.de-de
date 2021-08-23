---
title: force_allocate-Attribut
description: Das ACF-Attribut \force \_ allocate\ erzwingt, dass ein Zeigerparameter mithilfe von midl user allocate zugeordnet wird, \_ \_ anstatt die Zuordnung zu optimieren.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate-Attribut MIDL
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c82e1665e4c49461c3c7bd1c315b31f4f72c7e3f0e5331d9f0326347d36105
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582160"
---
# <a name="force_allocate-attribute"></a>Zuordnen des Attributs erzwingen \_

Die \[ **ACF-Attributerzwingung \_ erzwingt,** \] dass ein Zeigerparameter mithilfe von [**midl user \_ \_ allocate**](midl-user-allocate-1.md) zugeordnet wird, anstatt die Zuordnung zu optimieren.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a>Parameter

Dieses Attribut verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

RPC versucht, Speicherbelegungen auf dem Server zu minimieren, indem Zeiger auf interne Speicherpuffer bereitgestellt werden. Dieser Ansatz kann Probleme für Anwendungen verursachen, die versuchen, [**midl \_ user \_ free**](midl-user-free-1.md) direkt auf RPC-bereitgestellten Zeigern aufzurufen, da ein optimierter Zeiger nicht freigegeben werden kann. Das Markieren eines Parameters mit **\[ "Force \_ Allocate" \]** verhindert diese Optimierung für alle Zeiger, die ihn ableiten.

Eine weitere häufige Verwendung von **\[ Force \_ Allocate \]** besteht darin, die Ausrichtung des Arbeitsspeichers zu gewährleisten, auf den gezeigt wird, wenn eine Anwendung eine Ausrichtung erfordert, die größer als die des Arbeitsspeichers ist, auf den gezeigt wird. Beispielsweise übergeben Anwendungen Daten häufig in einem generischen Bytearray, anstatt den tatsächlichen Typ zu verwenden. Es ist jedoch garantiert, dass ein Byte nur bei 1 ausgerichtet wird. Dies kann zu Problemen bei Anwendungen führen, die eine größere Ausrichtung voraussetzen. Durch Markieren des Parameters mit **\[ force \_ allocate \]** kann die Anwendung sicherstellen, dass der gesamte Arbeitsspeicher, auf den gezeigt wird, eine Ausrichtung aufweist, die der von [**der mittleren \_ \_ Benutzerzuweisung**](midl-user-allocate-1.md)garantierten Entspricht.

## <a name="examples"></a>Beispiele

``` syntax
/* IDL file */
void Func1([in, out, string] char **ppstr);
void Func2([in] long s, [in, size_is(s)] byte *pData);

/* ACF file */

/* e.g. The application wishes to call midl_user_free on *ppstr and supply a new pointer */
Func1([force_allocate] pstr);

/* e.g. pData really points to a structure that needs an alignment greater than 1 */
Func2([force_allocate] pData);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vermeiden des Ausblendens von Informationen](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[Entwerfen von 64-Bit-kompatiblen Schnittstellen](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[**midl \_ user \_ allocate**](midl-user-allocate-1.md)
</dt> <dt>

[**midl \_ user \_ free**](midl-user-free-1.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> </dl>

 

 