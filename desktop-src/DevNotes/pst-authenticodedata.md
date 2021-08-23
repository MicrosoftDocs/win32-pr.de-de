---
description: Definiert Daten, die bei der Microsoft Authenticode-Überprüfung von Elementdaten verwendet werden sollen.
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: PST_AUTHENTICODEDATA -Struktur (Pstore.h)
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
ms.openlocfilehash: abf5bc69fd36e45cc715b3805f5407e821cfc7efc7f6595bcfc9eab8d762b716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690860"
---
# <a name="pst_authenticodedata-structure"></a>PST \_ AUTHENTICODEDATA-Struktur

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]

Definiert Daten, die bei der Microsoft Authenticode-Überprüfung von Elementdaten verwendet werden sollen.

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

**cbSize**
</dt> <dd>

Die Größe dieser Struktur.

</dd> <dt>

**dwModifiers**
</dt> <dd>

Ein -Wert, der den Modifizierer identifiziert, den einer einer Kette von Aufrufern überprüfen muss.



| Wert                                                                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <dt>**PST \_ AC \_ SINGLE \_ CALLER**</dt> <dt>0</dt> </dl>           | Nur eine einzelne Ebene in der Aufrufkette für PStore. Der Aufrufer besteht die Überprüfung. Das angegebene Bild ist der direkte Aufrufer und eine Anwendung (.exe).<br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <dt>**PST \_ AC \_ TOP \_ LEVEL \_ CALLER**</dt> <dt>1</dt> </dl> | Der Aufrufer der obersten Ebene muss die Überprüfung bestehen, es kann jedoch Zwischen-DLLs geben. Das angegebene Image ist nicht notwendigerweise der direkte Aufrufer und eine Anwendung (.exe).<br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <dt>**PST \_ AC \_ IMMEDIATE \_ CALLER**</dt> <dt>2</dt> </dl>  | Der direkte Aufrufer muss die Überprüfung bestehen, muss aber nicht der Prozess der obersten Ebene sein. Das angegebene Image ist der direkte Aufrufer, und das Image kann eine Anwendung (.exe) oder eine DLL sein.<br/> |



 

</dd> <dt>

**szRootCA**
</dt> <dd>

Ein Zeiger auf eine Breitzeichenzeichenfolge, die die Stammzertifizierungsstelle für das Zertifikat darstellt; Verwenden **Sie NULL,** um eine beliebige verfügbare Zertifizierungsstelle zu verwenden.

</dd> <dt>

**szIssuer**
</dt> <dd>

Ein Zeiger auf eine Breitzeichenfolge, die die Zertifizierungsstelle darstellt, die das Zertifikat ausgestellt hat. Verwenden **Sie NULL,** um eine beliebige verfügbare Zertifizierungsstelle zu verwenden.

</dd> <dt>

**szPublisher**
</dt> <dd>

Ein Zeiger auf eine Breitzeichenfolge, die den Softwareherausgeber darstellt. Verwenden **Sie NULL,** um eine beliebige verfügbare Zertifizierungsstelle zu verwenden.

</dd> <dt>

**szProgramName**
</dt> <dd>

Ein Zeiger auf eine Breitzeichenfolge, die den Programmnamen darstellt; Verwenden **Sie NULL,** um eine beliebige verfügbare Zertifizierungsstelle zu verwenden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl> |



 

 
