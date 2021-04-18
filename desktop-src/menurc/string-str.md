---
title: Zeichen folgen Struktur
description: Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Sie enthält eine Zeichenfolge, die einen bestimmten Aspekt einer Datei beschreibt, z. b. die Version einer Datei, die Copyright Hinweise oder ihre Marken.
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- Zeichen folgen Struktur-Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7035223082a9e446caebd6e07d3d55c84536d09f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337302"
---
# <a name="string-structure"></a>Zeichen folgen Struktur

Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Sie enthält eine Zeichenfolge, die einen bestimmten Aspekt einer Datei beschreibt, z. b. die Version einer Datei, die Copyright Hinweise oder ihre Marken.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  WORD  Value;
} String;
```



## <a name="members"></a>Member

<dl> <dt>

**wlength**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Länge dieser **Zeichen** folgen Struktur in Bytes.

</dd> <dt>

**wvaluelength**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Größe des **Wertmembers** in Wörtern.

</dd> <dt>

**wType**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Der Typ der Daten in der Versions Ressource. Dieser Member ist 1, wenn die Versions Ressource Textdaten enthält, und 0, wenn die Versions Ressource binäre Daten enthält.

</dd> <dt>

**szkey**
</dt> <dd>

Typ: **WCHAR**

</dd> <dd>

Eine beliebige Unicode-Zeichenfolge. Der **szkey** -Member kann einen oder mehrere der folgenden Werte aufweisen. Diese Werte sind nur Richtlinien.

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Iny**


</dt> <dd>

Der **Wert** Mitglied enthält alle zusätzlichen Informationen, die zu Diagnose Zwecken angezeigt werden sollen. Diese Zeichenfolge kann eine beliebige Länge aufweisen.

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**CompanyName**


</dt> <dd>

Der **Wert** Mitglied identifiziert das Unternehmen, das die Datei erstellt hat. Beispiel: "Microsoft Corporation" oder "Standard Microsystems Corporation, Inc."

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**


</dt> <dd>

Das **Wertmember** beschreibt die Datei so, dass Sie Benutzern angezeigt werden kann. Diese Zeichenfolge wird möglicherweise in einem Listenfeld angezeigt, wenn der Benutzer die zu installierenden Dateien auswählt. Beispiel: "Tastaturtreiber für im Stil Formatierungs Tastatur" oder "Microsoft Word für Windows".

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**File Version**


</dt> <dd>

Der **Wertmember** identifiziert die Version dieser Datei. Der **Wert** könnte z. b. "3.00 a" oder "5.00. RC2" lauten.

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**


</dt> <dd>

Der **Wertmember** identifiziert den internen Namen der Datei, sofern vorhanden. Diese Zeichenfolge kann z. b. den Modulnamen für eine DLL, den Namen eines virtuellen Geräts für ein virtuelles Windows-Gerät oder einen Gerätenamen für einen MS-DOS-Gerätetreiber enthalten.

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**


</dt> <dd>

Der **Wert** Mitglied beschreibt alle Copyright Hinweise, Marken und registrierten Marken, die auf die Datei angewendet werden. Dies sollte den vollständigen Text aller Hinweise, rechtliche Symbole, Copyright-Datumsangaben, Markennummern usw. umfassen. In englischer Sprache sollte diese Zeichenfolge das folgende Format aufweisen: "Copyright Microsoft Corp. 1990 1994".

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**Legalmarken**


</dt> <dd>

Der **Wert** Mitglied beschreibt alle Marken und registrierten Marken, die auf die Datei angewendet werden. Dies sollte den vollständigen Text aller Hinweise, rechtliche Symbole, Markennummern usw. umfassen. Im Deutschen sollte diese Zeichenfolge das folgende Format aufweisen: "Windows ist eine Marke der Microsoft Corporation".

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**Optio**


</dt> <dd>

Das **Wertmember** identifiziert den ursprünglichen Namen der Datei ohne einen Pfad. Dadurch kann eine Anwendung ermitteln, ob eine Datei von einem Benutzer umbenannt wurde. Dieser Name ist möglicherweise nicht MS-DOS 8,3-Format, wenn die Datei für ein nicht-FAT-Dateisystem spezifisch ist.

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**


</dt> <dd>

Das **Wertmember** beschreibt, von wem, wo und warum diese private Version der Datei erstellt wurde. Diese Zeichenfolge sollte nur vorhanden sein, wenn das **vs \_ FF \_ PrivateBuild** -Flag im **dwFileFlags** -Member der [**vs \_ FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) -Struktur festgelegt ist. Der **Wert** könnte z. b. "von Oscar auf \\ OSCAR2 erstellt" lauten.

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**ProductName**


</dt> <dd>

Der **Wertmember** identifiziert den Namen des Produkts, mit dem diese Datei verteilt wird. Diese Zeichenfolge könnte z. b. "Microsoft Windows" lauten.

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**


</dt> <dd>

Das **Wertmember** identifiziert die Version des Produkts, mit dem diese Datei verteilt wird. Der **Wert** könnte z. b. "3.00 a" oder "5.00. RC2" lauten.

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**


</dt> <dd>

Das **Wertmember** beschreibt, wie sich diese Version der Datei von der normalen Version unterscheidet. Dieser Eintrag sollte nur vorhanden sein, wenn das **vs \_ FF \_ SpecialBuild** -Flag im **dwFileFlags** -Member der [**vs \_ FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) -Struktur festgelegt ist. Der **Wert** könnte z. b. "private Build for Olivetti lösen von Maus Problemen auf M250 und M250E Computers" lauten.

</dd> </dl> </dd> <dt>

**Auffüllen**
</dt> <dd>

Typ: **Word**

</dd> <dd>

So viele Null-Wörter, wie erforderlich, um den **Wertmember** an einer 32-Bit-Grenze auszurichten.

</dd> <dt>

**Wert**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Eine NULL terminierte Zeichenfolge. Weitere Informationen finden Sie in der Beschreibung des **szkey** -Members.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur ist keine echte C-Sprachstruktur, da Sie Member variabler Länge enthält. Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versions Ressource erstellt und wird nicht in den Header Dateien angezeigt, die im Windows Software Development Kit (SDK) enthalten sind.

Eine **Zeichen** folgen Struktur kann einen **szkey** -Wert von haben, z. b. "CompanyName" und den **Wert** "Microsoft Corporation". Eine andere **Zeichen** folgen Struktur mit dem gleichen **szkey** -Wert könnte den **Wert** "Microsoft GmbH" enthalten. Dies kann vorkommen, wenn die zweite **Zeichen** folgen Struktur einer [**STRINGTABLE**](stringtable.md) -Struktur zugeordnet wäre, deren **szkey** -Wert 040704b0 ist, d. h. Deutsch/Unicode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**STRINGTABLE**](stringtable.md)
</dt> <dt>

[**VS \_ fixedfileingefo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[**Stringfileingefo**](stringfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Versionsinformationen](version-information.md)
</dt> </dl>

 

 





