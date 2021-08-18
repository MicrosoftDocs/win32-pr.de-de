---
title: Zeichenfolgenstruktur
description: Stellt die Organisation von Daten in einer Dateiversionsressource dar. Sie enthält eine Zeichenfolge, die einen bestimmten Aspekt einer Datei beschreibt, z. B. die Version einer Datei, ihre Urheberrechtshinweise oder ihre Marken.
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- Zeichenfolgenstrukturmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a6db2c10e981ae059a46e84e7abfc4d6dfc372fc3c75c76cfc20fd8a8f42735d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776730"
---
# <a name="string-structure"></a>Zeichenfolgenstruktur

Stellt die Organisation von Daten in einer Dateiversionsressource dar. Sie enthält eine Zeichenfolge, die einen bestimmten Aspekt einer Datei beschreibt, z. B. die Version einer Datei, ihre Urheberrechtshinweise oder ihre Marken.

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

**wLength**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Länge dieser Zeichenfolgenstruktur in **Bytes.**

</dd> <dt>

**wValueLength**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Größe des Value-Members in **Wörtern.**

</dd> <dt>

**wType**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Der Datentyp in der Versionsressource. Dieser Member ist 1, wenn die Versionsressource Textdaten enthält, und 0, wenn die Versionsressource Binärdaten enthält.

</dd> <dt>

**szKey**
</dt> <dd>

Typ: **WCHAR**

</dd> <dd>

Eine beliebige Unicode-Zeichenfolge. Der **szKey-Member** kann einer oder mehrere der folgenden Werte sein. Diese Werte sind nur Richtlinien.

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Kommentare**


</dt> <dd>

Das **Value-Member** enthält alle zusätzlichen Informationen, die zu Diagnosezwecken angezeigt werden sollen. Diese Zeichenfolge kann eine beliebige Länge haben.

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**Companyname**


</dt> <dd>

Das **Value-Mitglied** identifiziert das Unternehmen, das die Datei erstellt hat. Beispiel: "Microsoft Corporation" oder "Standard Microsystems Corporation, Inc."

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**


</dt> <dd>

Der **Value-Member** beschreibt die Datei so, dass sie Benutzern präsentiert werden kann. Diese Zeichenfolge kann in einem Listenfeld angezeigt werden, wenn der Benutzer zu installierende Dateien auswählt. Beispiel: "Tastaturtreiber für Tastaturen im AT-Stil" oder "Microsoft Word für Windows".

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**


</dt> <dd>

Der **Value-Member** identifiziert die Version dieser Datei. Der Wert **kann** beispielsweise "3.00A" oder "5.00.RC2" sein.

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**


</dt> <dd>

Das **Value-Member** identifiziert den internen Namen der Datei, sofern vorhanden. Diese Zeichenfolge kann beispielsweise den Modulnamen für eine DLL, einen Namen eines virtuellen Geräts für ein virtuelles Windows-Gerät oder einen Gerätenamen für einen MS-DOS-Gerätetreiber enthalten.

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**


</dt> <dd>

Das **Value-Mitglied** beschreibt alle Urheberrechtshinweise, Marken und registrierten Marken, die für die Datei gelten. Dies sollte den vollständigen Text aller Hinweise, rechtliche Symbole, Copyright-Datumsangaben, Markennummern usw. umfassen. Auf Englisch sollte diese Zeichenfolge das Format "Copyright Microsoft Corp. 1990 1994" haben.

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**Legal Zustempel**


</dt> <dd>

Das **Value-Mitglied** beschreibt alle Marken und registrierten Marken, die für die Datei gelten. Dies sollte den vollständigen Text aller Hinweise, rechtliche Symbole, Markennummern usw. umfassen. Im Deutschen sollte diese Zeichenfolge das folgende Format aufweisen: "Windows ist eine Marke der Microsoft Corporation".

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**


</dt> <dd>

Das **Value-Member** identifiziert den ursprünglichen Namen der Datei, ohne einen Pfad. Dadurch kann eine Anwendung bestimmen, ob eine Datei von einem Benutzer umbenannt wurde. Dieser Name darf nicht im MS-DOS 8.3-Format vorliegen, wenn die Datei für ein Nicht-FAT-Dateisystem spezifisch ist.

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**


</dt> <dd>

Der **Value-Member** beschreibt, von wem, wo und warum diese private Version der Datei erstellt wurde. Diese Zeichenfolge sollte nur vorhanden sein, wenn das **VS \_ FF \_ PRIVATEBUILD-Flag** im **dwFileFlags-Member** der [**VS \_ FIXEDFILEINFO-Struktur festgelegt**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) ist. Der Wert könnte **z.** B. "Built by WIES \\ onNOM2" sein.

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**Productname**


</dt> <dd>

Das **Value-Member** identifiziert den Namen des Produkts, mit dem diese Datei verteilt wird. Diese Zeichenfolge könnte beispielsweise "Microsoft Windows" sein.

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**Productversion**


</dt> <dd>

Der **Value-Member** identifiziert die Version des Produkts, mit dem diese Datei verteilt wird. Der Wert **kann** beispielsweise "3.00A" oder "5.00.RC2" sein.

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**


</dt> <dd>

Der **Value-Member** beschreibt, wie sich diese Version der Datei von der normalen Version unterscheidet. Dieser Eintrag sollte nur vorhanden sein, wenn das **VS \_ FF \_ SPECIALBUILD-Flag** im **dwFileFlags-Member** der [**VS \_ FIXEDFILEINFO-Struktur festgelegt**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) ist. Der Wert **könnte** z. B. "Privater Build für Die Lösung von Mausproblemen auf M250- und M250E-Computern" sein.

</dd> </dl> </dd> <dt>

**Auffüllen**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

So viele Nullwörter wie erforderlich, um das **Value-Member** an einer 32-Bit-Grenze auszurichten.

</dd> <dt>

**Wert**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Eine auf 0 (null) beendete Zeichenfolge. Weitere Informationen **finden Sie** in der SzKey-Memberbeschreibung.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur ist keine echte C-Sprachstruktur, da sie Member variabler Länge enthält. Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versionsressource erstellt und wird nicht in den Headerdateien angezeigt, die im Lieferumfang des Windows Software Development Kit (SDK) enthalten sind.

Eine **String-Struktur** kann den **szKey-Wert** z. B. "CompanyName" und den **Wert** "Microsoft Corporation" haben. Eine **andere String-Struktur** mit dem gleichen **szKey-Wert** kann den **Wert** "Microsoft GmbH" enthalten. This might occur if the second **String** structure were associated with a [**StringTable**](stringtable.md) structure whose **szKey** value is 040704b0   that is, German/Unicode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Stringtable**](stringtable.md)
</dt> <dt>

[**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Versionsinformationen](version-information.md)
</dt> </dl>

 

 





