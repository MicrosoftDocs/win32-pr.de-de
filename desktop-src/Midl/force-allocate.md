---
title: force_allocate-Attribut
description: Das ACF-Attribut \ Force Allocation \_ \ erzwingt, dass ein Zeiger Parameter mithilfe der Benutzer Zuordnung von mittlerer l zugewiesen wird, \_ \_ anstatt die Zuordnung zu optimieren.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate Attribut-Mittel l
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f73d0386d786e4d3004c78b1acccda7e9be8fc16
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472844"
---
# <a name="force_allocate-attribute"></a>Attribut "zuordnen" erzwingen \_

Mit der ACF-Attribut \[ **Erzwingung wird erzwungen \_** \] , dass ein Zeiger Parameter mithilfe der [**Mittel \_ \_**](midl-user-allocate-1.md) Wertzuordnung zugewiesen wird, anstatt die Zuordnung zu optimieren.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a>Parameter

Dieses Attribut hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

RPC versucht, Speicher Belegungen auf dem Server zu minimieren, indem Zeiger auf interne Speicherpuffer bereitgestellt werden. Diese Vorgehensweise kann Probleme bei Anwendungen verursachen, die versuchen, den [**\_ Benutzer \_ kostenlos**](midl-user-free-1.md) für die von RPC bereitgestellten Zeiger aufzurufen, da ein optimierter Zeiger nicht freigegeben werden kann. Wenn Sie einen Parameter mit " **\[ erzwingen" \_ zuweisen \]** , wird diese Optimierung für alle Zeiger, die ihn ableiten, verhindert.

Eine weitere häufige Verwendung für die **\[ Zwangs \_ \]** Zuordnungen besteht darin, die Ausrichtung des Speichers zu gewährleisten, auf den verwiesen wird, wenn eine Anwendung eine Ausrichtung erfordert, die größer ist als der Speicher, auf den verwiesen wird Beispielsweise übergeben Anwendungen häufig Daten in einem generischen Bytearray, anstatt den eigentlichen Typ zu verwenden, aber ein Byte wird nur bei 1 sichergestellt, was für Anwendungen, die eine größere Ausrichtung annehmen, zu Problemen führen kann. Durch Markieren des Parameters mit der Zuweisungs **\[ \_ Zuteilung \]** kann die Anwendung sicherstellen, dass für den gesamten Speicher, auf den verwiesen wird, eine Ausrichtung entspricht, die durch die [**\_ Benutzer \_**](midl-user-allocate-1.md)Zuordnungen garantiert wird.

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

[Vermeiden von Informationen ausblenden](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[Entwerfen von 64-Bit-kompatiblen Schnittstellen](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[**mittlere Benutzer Zuordnungen \_ \_**](midl-user-allocate-1.md)
</dt> <dt>

[**mittlerer l- \_ Benutzer \_ kostenlos**](midl-user-free-1.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> </dl>

 

 