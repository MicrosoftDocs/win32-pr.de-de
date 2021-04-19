---
description: Liest das angegebene Datenelement aus dem geschützten Speicher.
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: 'Ipstore:: ReadItem-Methode (pstore. h)'
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
ms.openlocfilehash: 0464ef06bc7c2842d0c8f9ff76e8174f05338919
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359734"
---
# <a name="ipstorereaditem-method"></a>Ipstore:: ReadItem-Methode

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

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

*Schlüssel* \[ in\]
</dt> <dd>

Der Speicherbereich des Anbieters.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ Schlüssel \_ aktueller \_ Benutzer**</dt> <dt>0x00000000</dt> </dl>    | Der Speicher wird im Abschnitt Aktueller Benutzer der Registrierung verwaltet.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ Key \_ local \_ Machine**</dt> <dt>0x00000001</dt> </dl> | Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.<br/> |



 

</dd> <dt>

*pitemtype* \[ in\]
</dt> <dd>

Ein Zeiger auf eine GUID, die den Datentyp des zu lesenden Elements identifiziert.

</dd> <dt>

*pitemsubtype* \[ in\]
</dt> <dd>

Ein Zeiger auf eine GUID, die den Daten Untertyp des zu lesenden Elements identifiziert.

</dd> <dt>

" *szitemname* \[ " in\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen enthält, der dem gespeicherten Datenelement zugewiesen ist.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Ein **DWORD** , das die Größe des Puffers angibt, der das gespeicherte Datenelement enthält.

</dd> <dt>

*pbData* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der das gespeicherte Datenelement enthält.

</dd> <dt>

*ppromptinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**PST- \_ promptinfo**](pst-promptinfo.md) -Struktur.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Gibt die Benutzeroberfläche und das Sicherheits Verhalten für den Lesevorgang an.

Die Flagwerte können mit einem logischen OR kombiniert werden.



| Wert                                                                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**PST \_ Uneingeschränktes \_ ItemData**</dt> <dt>0x00000004</dt> </dl> | Gibt an, dass der Datenstrom nicht sicher ist. Standardmäßig sind Element Aufrufe sicher.<br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <dt>**PST \_ \_Abfrage der Abfrage**</dt> <dt>0x00000008</dt> </dl>                            | Gibt an, dass die Bestätigung bei Erfolg zurückgegeben wird. Wenn die Benutzeroberfläche aktiviert ist, wird der Erfolg **PST \_ E \_ OK** zurückgegeben. Wenn die Benutzeroberfläche nicht aktiviert ist, wird der Wert **" \_ PST \_ E \_ Item** " zurückgegeben.<br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**PST \_ Keine \_ UI- \_ Migration**</dt> <dt>0x00000010</dt> </dl>                  | Zeigen Sie die Benutzeroberfläche nur an, wenn ein benutzerdefiniertes Kennwort erforderlich ist.<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT** -Wert. Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Wenn **ReadItem** erfolgreich abgeschlossen wird, ist die Anwendung dafür verantwortlich, den zurückgegebenen Datenpuffer mithilfe der [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) -Funktion freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ipstore**](ipstore.md)
</dt> <dt>

[**PST \_ promptinfo**](pst-promptinfo.md)
</dt> </dl>

 

 
