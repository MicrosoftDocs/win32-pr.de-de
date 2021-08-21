---
description: Löscht das angegebene Element aus dem geschützten Speicher.
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: IPStore::D eleteItem-Methode (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e99a2ec9b39b035b4a4af24aa18c2936decd399043cc507ed0bf279c5696fd53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667451"
---
# <a name="ipstoredeleteitem-method"></a>IPStore::D eleteItem-Methode

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, ist in nachfolgenden Versionen jedoch möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den verstärkten Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Löscht das angegebene Element aus dem geschützten Speicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteItem(
  [in]       PST_KEY         Key,
  [in] const GUID            *pItemType,
  [in] const GUID            *pItemSubType,
  [in]       LPCWSTR         szItemName,
  [in]       PPST_PROMPTINFO pPromptInfo,
  [in]       DWORD           dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ In\]
</dt> <dd>

Der Anbieterspeicherbereich.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ KEY \_ CURRENT \_ USER**</dt> <dt>0x00000000</dt> </dl>    | Der Speicher wird im aktuellen Benutzerabschnitt der Registrierung verwaltet.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ KEY \_ LOCAL \_ MACHINE**</dt> <dt>0x00000001</dt> </dl> | Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.<br/> |



 

</dd> <dt>

*pItemType* \[ In\]
</dt> <dd>

Ein Zeiger auf eine **GUID,** die den Datentyp des zu löschenden Elements identifiziert.

</dd> <dt>

*pItemSubType* \[ In\]
</dt> <dd>

Eine **GUID,** die den zu löschenden Elementuntertyp angibt.

</dd> <dt>

*szItemName* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die den Namen des zu löschende Elements enthält.

</dd> <dt>

*pPromptInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**PST \_ PROMPTINFO-Struktur.**](pst-promptinfo.md)

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Gibt die Benutzeroberfläche und das Sicherheitsverhalten für den Löschvorgang an.



| Wert                                                                                                                                                                                                                                             | Bedeutung                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**PST \_ KEINE \_ \_ BENUTZEROBERFLÄCHENMIGRATION**</dt> <dt>0x00000010</dt> </dl> | Zeigen Sie die Benutzeroberfläche nur an, wenn ein benutzerdefiniertes Kennwort erforderlich ist.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT-Wert.** Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> <dt>

[**PST \_ PROMPTINFO**](pst-promptinfo.md)
</dt> </dl>

 

 
