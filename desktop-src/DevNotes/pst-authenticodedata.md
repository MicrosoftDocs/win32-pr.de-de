---
description: Definiert die Daten, die in der Microsoft Authenticode-Überprüfung von Elementdaten verwendet werden sollen.
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: PST_AUTHENTICODEDATA Struktur (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_AUTHENTICODEDATA
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: ff53526febcc8eab1a95285ffa3dcb59fe628238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370088"
---
# <a name="pst_authenticodedata-structure"></a>PST- \_ authenticodedata-Struktur

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Definiert die Daten, die in der Microsoft Authenticode-Überprüfung von Elementdaten verwendet werden sollen.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD    cbSize;
  DWORD    dwModifiers;
  LPCWSTR  szRootCA;
  LPCWSTR  szIssuer;
  LPCWSTR  szPublisher;
  LPCWSTR  szProgramName;
} PST_AUTHENTICODEDATA, *PPST_AUTHENTICODE_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**CBSIZE**
</dt> <dd>

Die Größe dieser Struktur.

</dd> <dt>

**dwmodifier**
</dt> <dd>

Ein Wert, der den Modifizierer identifiziert, der von einer Kette von Aufrufern überprüft werden muss.



| Wert                                                                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <dt>**PST \_ AC \_ Single \_ Caller**</dt> <dt>0</dt> </dl>           | Nur eine einzelne Ebene in der Aufrufkette an den pstore. Der Aufrufer übergibt die Überprüfungs Überprüfung. Das angegebene Bild ist der unmittelbare Aufrufer, und ist eine Anwendung (. exe).<br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <dt>**PST \_ Rufer der \_ obersten \_ Ebene \_ der AC**</dt> <dt>1</dt> </dl> | Der Aufrufer der obersten Ebene muss die Überprüfung bestehen, es können jedoch zwischengeschaltete DLLs vorhanden sein. Das angegebene Bild ist nicht notwendigerweise der unmittelbare Aufrufer, und ist eine Anwendung (. exe).<br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <dt>**PST \_ AC \_ immediate \_**</dt> -Aufrufer <dt>2</dt> </dl>  | Der unmittelbare Aufrufer muss die Überprüfung bestehen, muss jedoch nicht der Prozess der obersten Ebene sein. Das angegebene Bild ist der unmittelbare Aufrufer, und das Bild kann eine Anwendung (. exe) oder eine DLL sein.<br/> |



 

</dd> <dt>

**szrootca**
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge mit breit Zeichen, die die Stamm Zertifizierungsstelle (Certification Authority, ca) für das Zertifikat darstellt. Verwenden Sie **null** , um beliebige verfügbare ZS zu verwenden.

</dd> <dt>

**szissuer**
</dt> <dd>

Ein Zeiger auf eine breit Zeichen-Zeichenfolge, die die Zertifizierungsstelle darstellt, die das Zertifikat ausgestellt hat. Verwenden Sie **null** , um beliebige verfügbare ZS zu verwenden.

</dd> <dt>

**szpublisher**
</dt> <dd>

Ein Zeiger auf eine breit Zeichen-Zeichenfolge, die den Software Herausgeber darstellt. Verwenden Sie **null** , um beliebige verfügbare ZS zu verwenden.

</dd> <dt>

**szprogramname**
</dt> <dd>

Ein Zeiger auf eine breit Zeichen-Zeichenfolge, die den Programmnamen darstellt. Verwenden Sie **null** , um beliebige verfügbare ZS zu verwenden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl> |



 

 
