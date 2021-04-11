---
description: Enthält Informationen für die cryptuidlgviewsignerinfo-Funktion.
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: CRYPTUI_VIEWSIGNERINFO_STRUCT Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_VIEWSIGNERINFO_STRUCT
- CRYPTUI_VIEWSIGNERINFO_STRUCTA
- CRYPTUI_VIEWSIGNERINFO_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: da150da6b5115e20a78a4edca64a5c9a97f66132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042252"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a>Cryptui \_ viewsignerinfo- \_ Struktur Struktur

\[Die **cryptui \_ viewsignerinfo \_** -Struktur ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Die **cryptui \_ viewsignerinfo \_** -Struktur Struktur enthält Informationen für die [**cryptuidlgviewsignerinfo**](cryptuidlgviewsignerinfo.md) -Funktion.

> [!Note]  
> Diese Struktur ist nicht in einer veröffentlichten Header Datei deklariert. Um diese Struktur zu verwenden, deklarieren Sie Sie im exakten Format.

 

## <a name="syntax"></a>Syntax


```C++
typedef struct tagCRYPTUI_VIEWSIGNERINFO_STRUCT {
  DWORD            dwSize;
  HWND             hwndParent;
  DWORD            dwFlags;
  LPCTSTR          szTitle;
  CMSG_SIGNER_INFO *pSignerInfo;
  HCRYPTMSG        hMsg;
  LPCSTR           pszOID;
  DWORD_PTR        dwReserved;
  DWORD            cStores;
  HCERTSTORE       *rghStores;
  DWORD            cPropSheetPages;
  LPCPROPSHEETPAGE rgPropSheetPages;
} CRYPTUI_VIEWSIGNERINFO_STRUCT, *PCRYPTUI_VIEWSIGNERINFO_STRUCT;
```



## <a name="members"></a>Member

<dl> <dt>

**dwSize**
</dt> <dd>

Die Größe (in Bytes) dieser Struktur.

</dd> <dt>

**hwndParent**
</dt> <dd>

Das Handle des Fensters, das als übergeordnetes Element des Dialog Felds angezeigt werden soll. Dieser Member kann **null** sein, wenn das Dialogfeld kein übergeordnetes Element aufweisen soll.

</dd> <dt>

**dwFlags**
</dt> <dd>

Ein Satz von Flags, der das Verhalten der [**cryptuidlgviewsignerinfo**](cryptuidlgviewsignerinfo.md) -Funktion ändert. Zurzeit sind keine Flags definiert, daher muss dieser Member 0 (null) sein.

</dd> <dt>

**sztitle**
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Titel enthält, der im Dialogfeld angezeigt werden soll. Wenn dieser Member **null** ist, wird ein Standard Titel verwendet.

</dd> <dt>

**psignerinfo**
</dt> <dd>

Ein Zeiger auf eine [**CMSG- \_ Signatur Geber \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) -Struktur, die die anzuzeigenden Signatur Geber Informationen enthält.

</dd> <dt>

**hmsg**
</dt> <dd>

Das Handle der Nachricht, aus der die Signatur Geber Informationen extrahiert wurden.

</dd> <dt>

**pszoid**
</dt> <dd>

Ein Zeiger auf eine mit NULL endende ANSI-Zeichenfolge, die die Zeichen folgen Darstellung des [*Objekt Bezeichners*](../secgloss/o-gly.md) (OID) enthält, der angibt, wofür das Zertifikat, das die Signatur durchgeführt hat, überprüft werden soll. Wenn diese z. b. aufgerufen wird, um die Signatur einer [*Zertifikat Vertrauens Liste (Certificate Trust List*](../secgloss/c-gly.md) , CTL) anzuzeigen, sollte die **szoid \_ KP \_ CTL- \_ Verwendungs \_ Signatur** -OID-Zeichenfolge übergeben werden. Wenn dieser Member **null** ist, wird das Zertifikat nicht für die Verwendung überprüft.

</dd> <dt>

**dwReserved**
</dt> <dd>

Dieser Parameter wird derzeit nicht verwendet. Dieser Member muss **null** sein.

</dd> <dt>

**cstores**
</dt> <dd>

Die Anzahl der Elemente im **rghstores** -Array.

</dd> <dt>

**rghstores**
</dt> <dd>

Ein Array von **HCERTSTORE** -Werten, die die anderen Zertifikat Speicher für die Suche nach dem Zertifikat darstellen, mit dem die Nachricht signiert wurde. Wenn dieser Member **null** ist, werden keine weiteren Speicher durchsucht. Der **cstores** -Member enthält die Anzahl der Elemente in diesem Array.

</dd> <dt>

**cpropsheetpages**
</dt> <dd>

Die Anzahl der Elemente im **rgpropsheetpages** -Array.

</dd> <dt>

**rgpropsheetpages**
</dt> <dd>

Ein Array von [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) -Struktur Zeigern, die alle zusätzlichen Seiten definieren, die im Standard Dialogfeld angezeigt werden sollen. Wenn dieser Member **null** ist, werden keine weiteren Seiten angezeigt. Der **cpropsheetpages** -Member enthält die Anzahl der Elemente in diesem Array.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                      |
| Unicode- und ANSI-Name<br/>   | **Cryptui \_ Viewsignerinfo \_ structw** (Unicode) und **cryptui \_ viewsignerinfo \_ Structa** (ANSI)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cryptuidlgviewsignerinfo**](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 
