---
description: Öffnet einen angegebenen Zertifikatspeicher.
ms.assetid: d6f398b4-dba6-4d84-b5eb-3c7737d17a6e
title: Store. Open-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d70c6410d0ecb8edb91aa722bcf6f35cb9536c3ed2b7f03c2d5cb141937aeb69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897805"
---
# <a name="storeopen-method"></a>Store. Open-Methode

\[Die **Open-Methode** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen die [**X509Store-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Open-Methode** öffnet einen [*angegebenen Zertifikatspeicher.*](../secgloss/c-gly.md) Standardmäßig werden der CAPICOM \_ CURRENT \_ USER \_ STORE-Speicherort und der CAPICOM \_ MY \_ STORE-Speicher als schreibgeschützt geöffnet.

## <a name="syntax"></a>Syntax


```VB
Store.Open( _
  [ ByVal StoreLocation ], _
  [ ByVal StoreName ], _
  [ ByVal OpenMode ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StoreLocation* \[ in, optional\]
</dt> <dd>

Ein Wert der [CAPICOM \_ STORE \_ LOCATION-Enumeration,](capicom-store-location.md) der den Speicherort des zu öffnenden Speichers angibt. Der Standardwert ist CAPICOM \_ CURRENT \_ USER \_ STORE. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**CAPICOM \_ ACTIVE \_ \_ DIRECTORY-BENUTZERSPEICHER \_**</dt> </dl> | Der Speicher ist ein Active Directory-Speicher. Es wird kein Fehler generiert, wenn ein Active Directory-Speicher als Lese-/Schreibzugriff geöffnet wird. Änderungen am Speicher werden jedoch nicht beibehalten. Zertifikate können active Directory-Speichern nicht hinzugefügt oder daraus entfernt werden.<br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**CAPICOM \_ CURRENT \_ USER \_ STORE**</dt> </dl>                             | Der Speicher ist ein aktueller Benutzerspeicher. Ein aktueller Benutzerspeicher kann ein Lese-/Schreibspeicher sein. Wenn dies der Wert ist, werden Änderungen am Inhalt des Speichers beibehalten.<br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**\_CAPICOM-SPEICHER \_ FÜR LOKALE \_ COMPUTER**</dt> </dl>                          | Der Speicher ist ein lokaler Computerspeicher. Lokale Computerspeicher können nur dann Lese-/Schreibspeicher sein, wenn der Benutzer über Lese-/Schreibberechtigungen verfügt. Wenn der Benutzer über Lese-/Schreibberechtigungen verfügt und der Speicher mit Lese-/Schreibzugriff geöffnet wird, werden Änderungen am Inhalt des Speichers beibehalten.<br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**\_CAPICOM-SPEICHER \_**</dt> </dl>                                                | Der Speicher ist ein Speicher. Änderungen am Inhalt des Speichers werden nicht beibehalten.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**CAPICOM \_ \_ \_ SMARTCARD-BENUTZERSPEICHER \_**</dt> </dl>                   | Der Store ist die Gruppe der aktuellen Smartcards. Eingeführt in CAPICOM 2.0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*StoreName* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die den Namen des zu öffnenden Systemzertifikatspeichers enthält. Der Standardwert ist CAPICOM \_ MY \_ STORE. Wenn der Speicher über ein Webskript geöffnet wird, ist der schräge Schrägstrich ( ) im \\ Namen nicht zulässig. Zusätzlich zu den vom System definierten Speichern können auch benutzerdefinierte Speicher geöffnet werden.

Dieser Parameter kann ein benutzerdefinierter Speicher oder einer der folgenden Systemzertifikatspeicher sein.



| Wert                                                                                                                                                                            | Bedeutung                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <dt>**CAPICOM \_ CA \_ STORE**</dt> </dl>          | ZS-Speicher. Dieser Speicher wird zum Speichern von Zwischenzertifikaten der Zertifizierungsstelle verwendet.<br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <dt>**CAPICOM \_ MY \_ STORE**</dt> </dl>          | Mein Store. Dieser Speicher wird für die persönlichen Zertifikate eines Benutzers verwendet.<br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <dt>**CAPICOM \_ OTHER \_ STORE**</dt> </dl> | AddressBook Store. Dieser Speicher wird verwendet, um die Zertifikate anderer zu speichern.<br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <dt>**\_CAPICOM-STAMMSPEICHER \_**</dt> </dl>    | Stammspeicher. Dieser Speicher wird verwendet, um die Stammzertifizierungsstelle und selbstsignierte, vertrauenswürdige Zertifikate zu speichern.<br/> |



 

</dd> <dt>

*OpenMode* \[ in, optional\]
</dt> <dd>

Ein Wert der [CAPICOM \_ STORE OPEN \_ \_ MODE-Enumeration,](capicom-store-open-mode.md) der den Offenen Modus des Speichers angibt. Der Standardwert ist CAPICOM \_ STORE \_ OPEN READ \_ \_ ONLY. Wenn der Speicher über ein Webskript geöffnet wird, wird dieser Wert zu CAPICOM \_ STORE OPEN EXISTING ONLY \_ \_ \_ erzwungen. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                           | Bedeutung                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <dt>**CAPICOM \_ STORE \_ OPEN \_ MAXIMUM \_ ALLOWED**</dt> </dl> | Öffnen Sie den Speicher im Lese-/Schreibmodus, wenn der Benutzer über Lese-/Schreibberechtigungen verfügt. Öffnen Sie andernfalls den Speicher im schreibgeschützten Modus.<br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <dt>**CAPICOM \_ STORE \_ OPEN \_ READ \_ ONLY**</dt> </dl>                   | Öffnen Sie den Speicher im schreibgeschützten Modus.<br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <dt>**CAPICOM \_ STORE \_ OPEN \_ READ \_ WRITE**</dt> </dl>                | Öffnen Sie den Speicher im Lese-/Schreibmodus.<br/>                                                                                     |



 

Die folgenden Flags können mithilfe eines logischen OR-Vorgangs mit den Werten in der vorherigen **Tabelle kombiniert** werden.



| Wert                                                                                                                                                                                                                              | Bedeutung                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <dt>**CAPICOM \_ STORE \_ OPEN \_ EXISTING \_ ONLY**</dt> </dl>          | Nur vorhandene Speicher öffnen; erstellen Sie keinen neuen Speicher. Eingeführt in CAPICOM 2.0.<br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <dt>**CAPICOM \_ STORE \_ OPEN \_ INCLUDE \_ ARCHIVED**</dt> </dl> | Schließen Sie archivierte Zertifikate ein, wenn Sie den Speicher verwenden. Eingeführt in CAPICOM 2.0.<br/>   |



 

Filialen an einigen Standorten können nur im schreibgeschützten Modus geöffnet werden. Dazu gehören alle Speicher in CAPICOM \_ LOCAL \_ MACHINE \_ STORE, für die der Benutzer nicht über Schreibberechtigungen verfügt. Versuche, einen Speicher als Lese-/Schreibspeicher ohne den richtigen Zugriff und die entsprechenden Berechtigungen zu öffnen, führen zum Fehler der **Open-Methode.** Active Directory-Speicher können ohne Fehler der **Open-Methode** als Lese-/Schreibspeicher geöffnet werden. Änderungen am Speicher werden jedoch nicht beibehalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn diese Methode in einem SmartCard-Speicher aufgerufen wird, können zusätzliche SmartCard-Benutzeroberflächen aufgerufen werden.

> [!IMPORTANT]
> Wenn diese Methode von einem Webskript aufgerufen wird, muss das Skript auf digitale Zertifikate auf dem lokalen Computer zugreifen. Wenn Sie zulassen, dass das Skript auf Ihre digitalen Zertifikate zutritt, hat die Website, von der aus das Skript ausgeführt wird, auch Zugriff auf alle persönlichen Informationen, die in den Zertifikaten gespeichert sind. Wenn diese Methode zum ersten Mal aus einer bestimmten Domäne aufgerufen wird, wird ein Dialogfeld generiert, in dem der Benutzer angeben muss, ob der Zugriff auf die Zertifikate zugelassen werden soll. Speicher, die über ein Webskript geöffnet werden, erzwingen automatisch das FLAG CAPICOM \_ STORE \_ OPEN EXISTING \_ \_ ONLY.

 

Wenn *StoreLocation* **CAPICOM \_ SMART CARD USER STORE \_ \_ \_ ist,** *wird StoreName* ignoriert. In diesem Fall liest CAPICOM alle Zertifikate aller verfügbaren Leser, die eine Smartcard enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Speicher**](store.md)
</dt> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**Schließen**](store-close.md)
</dt> </dl>

 

 
