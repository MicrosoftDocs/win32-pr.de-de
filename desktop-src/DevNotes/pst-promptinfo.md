---
description: Definiert das Aufforderungs Verhalten des geschützten Speicher, wenn eine Benutzeroberfläche angezeigt wird.
ms.assetid: 413bcb33-5fe9-4ba1-b65f-3e53a7cbf70c
title: PST_PROMPTINFO Struktur (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_PROMPTINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: da499ea3d6f5037e9f1e745771112840a462f11d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368423"
---
# <a name="pst_promptinfo-structure"></a>PST \_ promptinfo-Struktur

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Definiert das Aufforderungs Verhalten des geschützten Speicher, wenn eine Benutzeroberfläche angezeigt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD      cbSize;
  DWORD      dwPromptFlags;
  DWORD_PTR  hwndApp;
  LPCWSTR    szPrompt;
} PST_PROMPTINFO, *PPST_PROMPTINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**CBSIZE**
</dt> <dd>

Die Größe dieser Struktur.

</dd> <dt>

**dwpromptflags**
</dt> <dd>

Dieses Flag wird ignoriert.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="PST_PF_ALWAYS_SHOW"></span><span id="pst_pf_always_show"></span><dl> <dt>**PST \_ PF \_ \_ zeigt immer**</dt> <dt>0x00000001</dt> an </dl> | Fordert an, dass der Anbieter das Eingabe Aufforderungs Dialogfeld für den Benutzer anzeigt, auch wenn es für diesen Zugriff nicht erforderlich ist. <br/> |
| <span id="PST_PF_NEVER_SHOW"></span><span id="pst_pf_never_show"></span><dl> <dt>**PST \_ PF \_ \_ zeigt nie**</dt> <dt>0x00000002</dt> an </dl>    | Zeigen Sie dem Benutzer nicht das Dialogfeld für die Eingabeaufforderung an.<br/>                                                                 |



 

</dd> <dt>

**hwndApp**
</dt> <dd>

Das Handle für das übergeordnete Fenster für die Benutzeroberfläche. Das **hwndApp** -Element bestimmt, wo die Benutzeroberfläche angezeigt wird. Wenn **null** übermittelt wird, wird der Desktop als übergeordnetes Fenster betrachtet.

</dd> <dt>

**szprompt**
</dt> <dd>

Die Zeichenfolge der Eingabeaufforderung.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DeleteItem**](ipstore-deleteitem.md)
</dt> <dt>

[**OpenItem**](ipstore-openitem.md)
</dt> <dt>

[**"ReadItem"**](ipstore-readitem.md)
</dt> <dt>

[**Schreib Element**](ipstore-writeitem.md)
</dt> </dl>

 

 
