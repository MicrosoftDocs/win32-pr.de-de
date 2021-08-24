---
description: Enthält Informationen für die CryptUIDlgViewSignerInfo-Funktion.
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: CRYPTUI_VIEWSIGNERINFO_STRUCT-Struktur
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
ms.openlocfilehash: bf35b4475047548e1744174717c238e99c6a744c17ef2fa76ce48217a4fc72aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875860"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a>CRYPTUI \_ \_ VIEWSIGNERINFO-STRUKTUR

\[Die **CRYPTUI \_ VIEWSIGNERINFO-Struktur \_** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Die **CRYPTUI \_ VIEWSIGNERINFO-Struktur \_** enthält Informationen für die [**CryptUIDlgViewSignerInfo-Funktion.**](cryptuidlgviewsignerinfo.md)

> [!Note]  
> Diese Struktur wird nicht in einer veröffentlichten Headerdatei deklariert. Um diese Struktur zu verwenden, deklarieren Sie sie im genauen angezeigten Format.

 

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

Das Handle des Fensters, das dem Dialogfeld über-übergeordnetes Element sein soll. Dieser Member kann NULL **sein,** wenn das Dialogfeld kein übergeordnetes Element enthalten soll.

</dd> <dt>

**dwFlags**
</dt> <dd>

Ein Satz von Flags, der das Verhalten der [**CryptUIDlgViewSignerInfo-Funktion**](cryptuidlgviewsignerinfo.md) ändert. Derzeit sind keine Flags definiert, daher muss dieser Member 0 (null) sein.

</dd> <dt>

**szTitle**
</dt> <dd>

Ein Zeiger auf eine auf NULL terminierte Zeichenfolge, die den Titel enthält, der im Dialogfeld angezeigt werden soll. Wenn dieser Member NULL **ist,** wird ein Standardtitel verwendet.

</dd> <dt>

**pSignerInfo**
</dt> <dd>

Ein Zeiger auf eine [**CMSG \_ SIGNER \_ INFO-Struktur,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) die die anzuzeigenden Signaturinformationen enthält.

</dd> <dt>

**hMsg**
</dt> <dd>

Das Handle der Nachricht, aus der die Signatorinformationen extrahiert wurden.

</dd> <dt>

**pszOID**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte ANSI-Zeichenfolge, die die Zeichenfolgendarstellung des Objektbezeichners [](../secgloss/o-gly.md) (OID) enthält, die angibt, auf welches Zertifikat die Signatur überprüft werden soll. Wenn dies beispielsweise aufgerufen wird, um die Signatur einer Zertifikatvertrauensliste (Certificate [*Trust List,*](../secgloss/c-gly.md) CTL) anzeigen zu können, sollte die **OID-Zeichenfolge szOID \_ KP \_ CTL USAGE \_ \_ SIGNING** übergeben werden. Wenn dieser Member **NULL ist,** wird das Zertifikat nicht auf Verwendungen überprüft.

</dd> <dt>

**dwReserved**
</dt> <dd>

Dieser Parameter wird derzeit nicht verwendet. Dieser Member muss NULL **sein.**

</dd> <dt>

**cStores**
</dt> <dd>

Die Anzahl der Elemente im **rghStores-Array.**

</dd> <dt>

**rghStores**
</dt> <dd>

Ein Array von **HCERTSTORE-Werten,** die die anderen Zertifikatspeicher darstellen, die nach dem Zertifikat suchen, das die Nachricht signiert hat. Wenn dieser Member NULL **ist,** werden keine zusätzlichen Speicher durchsucht. Das **cStores-Element** enthält die Anzahl der Elemente in diesem Array.

</dd> <dt>

**cPropSheetPages**
</dt> <dd>

Die Anzahl der Elemente im **rgPropSheetPages-Array.**

</dd> <dt>

**rgPropSheetPages**
</dt> <dd>

Ein Array von [**PROPSHEETPAGE-Strukturze0ern,**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) die zusätzliche Seiten definieren, die im Standarddialogfeld angezeigt werden. Wenn dieser Member **NULL ist,** werden keine zusätzlichen Seiten angezeigt. Das **cPropSheetPages-Element** enthält die Anzahl der Elemente in diesem Array.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                      |
| Unicode- und ANSI-Name<br/>   | **CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTW** (Unicode) und **CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTA** (ANSI)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 
