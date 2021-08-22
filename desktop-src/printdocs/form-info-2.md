---
description: Enthält Informationen zu einem lokalisierbaren Druckformular.
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: FORM_INFO_2 -Struktur (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_2
- _FORM_INFO_2A
- _FORM_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: fd933bf0ace6f394a801ab8dc4ef1fa30344b47966c09865a3aa4b713c6f2ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971519"
---
# <a name="form_info_2-structure"></a>FORM \_ INFO \_ 2-Struktur

Enthält Informationen zu einem lokalisierbaren Druckformular.

## <a name="syntax"></a>Syntax


```C++
typedef struct _FORM_INFO_2 {
  DWORD   Flags;
  LPTSTR  pName;
  SIZEL   Size;
  RECTL   ImageableArea;
  LPCSTR  pKeyword;
  DWORD   StringType;
  LPCTSTR pMuiDll;
  DWORD   dwResourceId;
  LPCTSTR pDisplayName;
  LANGID  wLangId;
} FORM_INFO_2, *PFORM_INFO_2;
```



## <a name="members"></a>Member

<dl> <dt>

**Flags**
</dt> <dd>

Die Formulareigenschaften. Die folgenden Werte sind definiert, aber es kann nur einer festgelegt werden. Wenn **FORM \_ INFO \_ 2 von** [**GetForm**](getform.md) oder [**EnumForms**](enumforms.md)zurückgegeben wird, wird **Flags** auf den aktuellen Wert in der Formulardatenbank festgelegt.



| Wert         | Bedeutung                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_FORMULARBENUTZER    | Wenn dieses Bitflag festgelegt ist, wurde das Formular vom Benutzer definiert. Formulare, für die dieses Flag festgelegt ist, werden in der Registrierung definiert.                                                                                                                                                                    |
| FORMULAR \_ INTEGRIERT | Wenn dieses Bitflag festgelegt ist, ist das Formular Teil des Spoolers. Formulardefinitionen, für die dieses Flag festgelegt ist, werden nicht in der Registrierung angezeigt. Integrierte Formulare können nicht geändert werden, daher sollte dieses Flag nicht festgelegt werden, wenn die Struktur an [**AddForm**](addform.md) oder [**SetForm übergeben wird.**](setform.md) |
| \_FORMULARDRUCKER | Wenn dieses Bitflag festgelegt ist, wird das Formular einem bestimmten Drucker zugeordnet, und seine Definition wird in der Registrierung angezeigt.                                                                                                                                                                      |



 

</dd> <dt>

**pName**
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Formulars angibt. Der Formularname darf 31 Zeichen nicht überschreiten.

</dd> <dt>

**Größe**
</dt> <dd>

Die Breite und Höhe des Formulars in Tausendstel Millimetern.

</dd> <dt>

**ImageableArea**
</dt> <dd>

Die Breite und Höhe des Seitenbereichs in Tausendstel Millimeter, auf dem der Drucker drucken kann.

</dd> <dt>

**pKeyword**
</dt> <dd>

Ein Zeiger auf einen nicht lokalisierbaren Zeichenfolgenbezeichner des Formulars. Bei der Übergeben [**an AddForm**](addform.md) oder [**SetForm**](setform.md)bietet dies dem Aufrufer eine Möglichkeit, das Formular in allen Lokalen zu identifizieren.

</dd> <dt>

**StringType**
</dt> <dd>

Gibt an, wie ein lokalisierter Anzeigename für das Formular zur Laufzeit erhalten wird. Die folgenden Werte werden definiert. Nur eine kann in jedem Aufruf von [**AddForm**](addform.md) oder [**SetForm festgelegt werden.**](setform.md) SOWOHL STRING \_ STRINGDLL als auch STRING LANGPAIR können in form info \_ **\_ \_ 2** (s) festgelegt werden, die von [**GetForm**](getform.md) oder [**EnumForms zurückgegeben werden.**](enumforms.md) Siehe Hinweise.



| Wert            | Bedeutung                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| STRING \_ NONE     | Es gibt keinen lokalisierten Anzeigenamen.                                                                                                                                                            |
| STRING \_ STRINGDLL   | Der Anzeigename wird aus [](/windows/desktop/Intl/mui-resource-management) der in **pMuiDll** mehrsprachige Benutzeroberfläche lokalisierten Ressourcen-DLL extrahiert. Die ID befindet sich im **dwResourceId-Mitglied.** |
| STRING \_ LANGPAIR | Der Anzeigename und die Sprach-ID werden direkt von **pDisplayName** bereitgestellt, und die Sprache wird durch **wLangId angegeben.**                                                                       |



 

</dd> <dt>

**pMuiDll**
</dt> <dd>

Die [mehrsprachige Benutzeroberfläche](/windows/desktop/Intl/mui-resource-management) lokalisierte Ressourcen-DLL, die den lokalisierten Anzeigenamen enthält.

</dd> <dt>

**dwResourceId**
</dt> <dd>

Die Ressourcen-ID des Anzeigenamens des Formulars in **pMuiDll**.

</dd> <dt>

**pDisplayName**
</dt> <dd>

Der Anzeigename des Formulars in der durch **wLangId angegebenen Sprache.**

</dd> <dt>

**wLangId**
</dt> <dd>

Die Sprache von **pDisplayName.**

</dd> </dl>

## <a name="remarks"></a>Hinweise

Bei einem Aufruf von [**AddForm oder**](addform.md) [**SetForm:**](setform.md)

-   Wenn **StringType** STRING NONE ist, müssen \_ sowohl **pMuiDll** als auch **pDisplayName** **NULL** und **dwResourceId** und **wLangId** 0 sein.
-   Wenn **StringType** STRING \_ STRINGDLL ist, **muss pDisplayName** **NULL** und **wLangId** 0 sein.
-   Wenn **StringType** STRING \_ LANGPAIR ist, **muss pMuiDll** **NULL** und **dwResourceId** 0 sein.

Für form **\_ info \_ 2,** die durch einen Aufruf von [**GetForm**](getform.md) oder [**EnumForms zurückgegeben wird:**](enumforms.md)

-   Wenn **StringType sowohl** STRING WRDLL als auch \_ STRING \_ LANGPAIR ist, verfügen **pMuiDll**, **pDisplayName,** **dwResourceId** und **wLangId** über gültige Werte.
-   Wenn **StringType nur** STRING \_ STRINGDLL ist, **verfügen pMuiDll** und **dwResourceId** über gültige Werte. **pDisplayName** ist **NULL und** **wLangId** ist 0.
-   Wenn **StringType nur** STRING \_ LANGPAIR ist, verfügen **pDisplayName** und **wLangId** über gültige Werte. **pMuiDll ist** **NULL** und **dwResourceId** ist 0.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ FORM \_ INFO \_ 2W** (Unicode) und **\_ FORM INFO \_ \_ 2A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[Multilingual User Interface](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**EnumForms**](enumforms.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

