---
description: Schreibt ein Datenelement in den geschützten Speicher.
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: IPStore::WriteItem-Methode (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d8af896d2aca8ae218ba06f94cb0e2ef5f86fc4122acf3463356f5fea3dafd1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955889"
---
# <a name="ipstorewriteitem-method"></a>IPStore::WriteItem-Methode

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]

Schreibt ein Datenelement in den geschützten Speicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT WriteItem(
  [in]        PST_KEY        Key,
  [in]  const GUID           *pItemType,
  [in]  const GUID           *pItemSubtype,
  [in]        LPCWSTR        *szItemName,
  [out]       DWORD          *cbData,
  [out]       BYTE           ppbData,
  [in]        PPST_PROMPTIFO pProomptInfo,
  [in]        DWORD          dwDefaultConfirmationStyle,
  [in]        DWORD          dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ In\]
</dt> <dd>

Der Speicherbereich des Anbieters.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ KEY \_ CURRENT \_ USER**</dt> <dt>0X00000000</dt> </dl>    | Der Speicher wird im aktuellen Benutzerabschnitt der Registrierung verwaltet.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ KEY \_ LOCAL \_ MACHINE**</dt> <dt>0X00000001</dt> </dl> | Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.<br/> |



 

</dd> <dt>

*pItemType* \[ In\]
</dt> <dd>

Ein Zeiger auf eine **GUID,** die den Datentyp des zu schreibenden Datenelements identifiziert.

</dd> <dt>

*pItemSubtype* \[ In\]
</dt> <dd>

Ein Zeiger auf eine **GUID,** die den Datenuntertyp des zu schreibenden Datenelements identifiziert.

</dd> <dt>

*szItemName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen enthält, der dem gespeicherten Datenelement zugewiesen ist.

</dd> <dt>

*cbData* \[ out\]
</dt> <dd>

Ein Zeiger auf ein **DWORD,** das die Größe des Puffers angibt, der das gespeicherte Datenelement enthält.

</dd> <dt>

*ppbData* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der das zu schreibende Datenelement enthält.

</dd> <dt>

*pProomptInfo* \[ In\]
</dt> <dd>

Zeiger auf eine [**PST \_ PROMPTINFO-Struktur.**](pst-promptinfo.md)

</dd> <dt>

*dwDefaultConfirmationStyle* \[ In\]
</dt> <dd>

Der Standardbestätigungsstil.



| Wert                                                                                                                                                                                                                             | Bedeutung                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <dt>**PST \_ CF \_ DEFAULT**</dt> <dt>0x00000000</dt> </dl> | Ermöglicht dem Benutzer die Auswahl des Bestätigungsstils. <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <dt>**PST \_ CF \_ NONE-0x00000001**</dt> <dt></dt> </dl>          | Erzwingt die automatische Elementerstellung. <br/>                      |



 

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Die Benutzeroberfläche und das Sicherheitsverhalten für den Schreibvorgang.



| Wert                                                                                                                                                                                                                                                              | Bedeutung                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <dt>**PST \_ KEINE \_ ÜBERSCHREIBUNG**</dt> <dt>0x00000002</dt> </dl>                            | Gibt an, dass das Element im geschützten Speicher erstellt werden soll. Das Überschreiben eines vorhandenen Elements ist nicht mehr zu sehen.<br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**PST \_ UNRESTRICTED \_ ITEMDATA**</dt> <dt>0x00000004</dt> </dl> | Gibt an, dass der Datenstrom nicht sicher ist. Standardmäßig sind Elementaufrufe sicher.<br/>                         |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT-Wert.** Der Wert **PST E OK gibt \_ \_ an,** dass die Funktion erfolgreich war.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> <dt>

[**PST \_ PROMPTINFO**](pst-promptinfo.md)
</dt> </dl>

 

 
