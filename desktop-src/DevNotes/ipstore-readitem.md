---
description: Liest das angegebene Datenelement aus dem geschützten Speicher.
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: IPStore::ReadItem-Methode (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 516eb55772e375d09d3b134dee456c090cf11d6ef0d10905f99a822b1df0d9e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001489"
---
# <a name="ipstorereaditem-method"></a>IPStore::ReadItem-Methode

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, ist aber in nachfolgenden Versionen möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den verstärkten Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Liest das angegebene Datenelement aus dem geschützten Speicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReadItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       DWORD          cbData,
  [in]       BYTE_RPC_FAR   *pbData,
  [in]       PPST_PROMPTIFO pPromptInfo,
  [in]       DWORD          dwFlags
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

Ein Zeiger auf eine GUID, die den Datentyp des zu lesenden Elements identifiziert.

</dd> <dt>

*pItemSubtype* \[ In\]
</dt> <dd>

Ein Zeiger auf eine GUID, die den Datenuntertyp des zu lesenden Elements identifiziert.

</dd> <dt>

*szItemName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den dem gespeicherten Datenelement zugewiesenen Namen enthält.

</dd> <dt>

*cbData* \[ In\]
</dt> <dd>

Ein **DWORD,** das die Größe des Puffers angibt, der das gespeicherte Datenelement enthält.

</dd> <dt>

*pbData* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der das gespeicherte Datenelement enthält.

</dd> <dt>

*pPromptInfo* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**PST \_ PROMPTINFO-Struktur.**](pst-promptinfo.md)

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Gibt die Benutzeroberfläche und das Sicherheitsverhalten für den Lesevorgang an.

Die Flagwerte können mit einem logischen OR kombiniert werden.



| Wert                                                                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**PST \_ UNRESTRICTED \_ ITEMDATA**</dt> <dt>0x00000004</dt> </dl> | Gibt an, dass der Datenstrom unsicher ist. Standardmäßig sind Elementaufrufe sicher.<br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <dt>**PST \_ PROMPT \_ QUERY**</dt> <dt>0x00000008</dt> </dl>                            | Gibt an, dass die Bestätigung bei Erfolg zurückgegeben wird. Wenn die Benutzeroberfläche aktiviert ist, wird der Erfolg von **PST \_ E \_ OK** zurückgegeben. Wenn die Benutzeroberfläche nicht aktiviert ist, wird der Wert **PST \_ E ITEM \_ \_ EXISTS** zurückgegeben.<br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**PST \_ KEINE \_ \_ BENUTZEROBERFLÄCHENMIGRATION**</dt> <dt>0x00000010</dt> </dl>                  | Zeigen Sie die Benutzeroberfläche nur an, wenn ein benutzerdefiniertes Kennwort erforderlich ist.<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT-Wert.** Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.

## <a name="remarks"></a>Hinweise

Wenn **ReadItem** erfolgreich abgeschlossen wird, ist die Anwendung für die Freigabe des zurückgegebenen Datenpuffers mithilfe der [**CoTaskMemFree-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) verantwortlich.

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

 

 
