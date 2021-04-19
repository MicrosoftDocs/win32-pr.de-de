---
description: Öffnet einen angegebenen Zertifikat Speicher.
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
ms.openlocfilehash: ef4ffe89a4b726ecfa33fb95d213d809cae2487b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354122"
---
# <a name="storeopen-method"></a>Store. Open-Methode

\[Die **Open** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Store-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Open** -Methode öffnet einen angegebenen [*Zertifikat Speicher*](../secgloss/c-gly.md). Standardmäßig werden der Speicherort für den aktuellen CAPICOM \_ \_ \_ -Benutzer Speicherort und der CAPICOM- \_ \_ Speicher für mein Geschäft als schreibgeschützt geöffnet.

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

*Storeloation* \[ in, optional\]
</dt> <dd>

Ein Wert der [CAPICOM \_ Store \_ Location](capicom-store-location.md) -Enumeration, der den Speicherort des zu öffnenden Stores angibt. Der Standardwert ist "CAPICOM \_ Current \_ User \_ Store". Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**CAPICOM \_ Active \_ Directory- \_ Benutzer \_ Speicher**</dt> </dl> | Der Speicher ist ein Active Directory Speicher. Wenn ein Active Directory Speicher als Lese-/Schreibzugriff geöffnet ist, wird kein Fehler generiert, aber alle Änderungen am Speicher werden nicht beibehalten. Zertifikate können Active Directory speichern nicht hinzugefügt oder daraus entfernt werden.<br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**CAPICOM \_ aktueller \_ Benutzer \_ Speicher**</dt> </dl>                             | Der Speicher ist ein aktueller Benutzerspeicher. Ein aktueller Benutzerspeicher kann ein Lese-/Schreibspeicher sein. Wenn dies der Fall ist, werden Änderungen am Inhalt des Stores persistent gespeichert.<br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**lokaler CAPICOM- \_ \_ Computer \_ Speicher**</dt> </dl>                          | Der Speicher ist ein lokaler Computerspeicher. Lokale Computerspeicher können nur Lese-/Schreibspeicher sein, wenn der Benutzer über Lese-/Schreibberechtigungen verfügt. Wenn der Benutzer über Lese-/Schreibberechtigungen verfügt und der Speicher mit Lese-/Schreibzugriff geöffnet wird, werden Änderungen im Inhalt des Stores beibehalten.<br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**CAPICOM- \_ Speicher Speicher \_**</dt> </dl>                                                | Der Speicher ist ein Speicher Speicher. Alle Änderungen im Inhalt des Stores werden nicht persistent gespeichert.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**CAPICOM \_ - \_ Smartcard- \_ Benutzer \_ Speicher**</dt> </dl>                   | Der Speicher ist die Gruppe der vorhandenen Smartcards. Eingeführt in CAPICOM 2,0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*StoreName* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die den Namen des zu öffnenden Systemzertifikat Speicher enthält. Der Standardwert ist "CAPICOM \_ My \_ Store". Wenn der Speicher von einem Webskript aus geöffnet wird, ist der umgekehrte Schrägstrich ( \\ ) im Namen nicht zulässig. Zusätzlich zu den durch das System definierten speichern können benutzerdefinierte Speicher geöffnet werden.

Dieser Parameter kann ein benutzerdefinierter Speicher oder einer der folgenden Systemzertifikat Speicher sein.



| Wert                                                                                                                                                                            | Bedeutung                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <dt>**CAPICOM- \_ ca- \_ Speicher**</dt> </dl>          | CA-Speicher. Dieser Speicher wird zum Speichern von zwischen Zertifizierungsstellen-Zertifikaten verwendet.<br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <dt>**CAPICOM \_ mein \_ Geschäft**</dt> </dl>          | Mein Geschäft. Dieser Speicher wird für die persönlichen Zertifikate eines Benutzers verwendet.<br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <dt>**CAPICOM \_ anderer \_ Speicher**</dt> </dl> | Addressbook-Speicher. Dieser Speicher wird verwendet, um die Zertifikate anderer Benutzer beizubehalten.<br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <dt>**CAPICOM-Stamm \_ \_ Speicher**</dt> </dl>    | Stamm Speicher. Dieser Speicher wird verwendet, um die Stamm Zertifizierungsstelle und selbst signierte vertrauenswürdige Zertifikate zu speichern.<br/> |



 

</dd> <dt>

*OpenMode* \[ in, optional\]
</dt> <dd>

Ein Wert der-Enumeration des [CAPICOM- \_ Speicher \_ öffnenden \_ Modus](capicom-store-open-mode.md) , der den Öffnungs Modus des Stores angibt. Der Standardwert ist "CAPICOM \_ Store \_ Open \_ Read \_ only". Wenn der Speicher von einem Webskript aus geöffnet wird, wird dieser Wert erzwungen, dass der CAPICOM- \_ Speicher \_ nur geöffnet ist \_ \_ . Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                           | Bedeutung                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <dt>**\_ \_ \_ maximal zulässige Anzahl geöffneter CAPICOM-Speicher \_**</dt> </dl> | Öffnen Sie den Speicher im Lese-/Schreibmodus, wenn der Benutzer über Lese-/Schreibberechtigungen verfügt. Andernfalls öffnen Sie den Speicher im schreibgeschützten Modus.<br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <dt>**CAPICOM \_ Store \_ Open \_ Read \_ Only**</dt> </dl>                   | Öffnen Sie den Speicher im schreibgeschützten Modus.<br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <dt>**CAPICOM \_ Store \_ offene \_ Lese- \_ /Schreibzugriff**</dt> </dl>                | Öffnen Sie den Speicher im Lese-/Schreibmodus.<br/>                                                                                     |



 

Die folgenden Flags können mit den Werten in der vorherigen Tabelle mithilfe einer logischen **or** -Operation kombiniert werden.



| Wert                                                                                                                                                                                                                              | Bedeutung                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <dt>**CAPICOM \_ - \_ Speicher \_ Öffnen \_ nur vorhanden**</dt> </dl>          | Nur vorhandene Speicher öffnen; Erstellen Sie keinen neuen Speicher. Eingeführt in CAPICOM 2,0.<br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <dt>**CAPICOM \_ Store \_ Open \_ include \_ archiviert**</dt> </dl> | Schließt Archivierte Zertifikate ein, wenn der Speicher verwendet wird. Eingeführt in CAPICOM 2,0.<br/>   |



 

Filialen an manchen Speicherorten können nur im schreibgeschützten Modus geöffnet werden. Hierzu gehören alle Filialen im lokalen CAPICOM- \_ \_ Computer \_ Speicher, für die der Benutzer nicht über Schreibberechtigungen verfügt. Wenn versucht wird, einen Speicher ohne angemessenen Zugriff als Lese-/Schreibspeicher zu öffnen, führt dies zu einem Fehler bei der **Open** -Methode. Active Directory Stores können als Lese-/Schreibspeicher geöffnet werden, ohne dass die **Open** -Methode ausfällt, Änderungen am Speicher werden jedoch nicht beibehalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn diese Methode in einem smartcardspeicher aufgerufen wird, können zusätzliche Smartcard-Benutzeroberflächen aufgerufen werden.

> [!IMPORTANT]
> Wenn diese Methode von einem Webskript aufgerufen wird, muss das Skript auf die digitalen Zertifikate auf dem lokalen Computer zugreifen. Wenn Sie zulassen, dass das Skript auf Ihre digitalen Zertifikate zugreift, erhält die Website, von der aus das Skript ausgeführt wird, auch Zugriff auf alle persönlichen Informationen, die in den Zertifikaten gespeichert sind. Wenn diese Methode zum ersten Mal von einer bestimmten Domäne aufgerufen wird, wird ein Dialogfeld generiert, in dem der Benutzer angeben muss, ob der Zugriff auf die Zertifikate zulässig sein soll. Speicher, die von einem Webskript geöffnet wurden, erzwingen automatisch, dass das CAPICOM- \_ Speicher-Flag " \_ \_ vorhandenes \_

 

Handelt es sich bei *storeloation* um **CAPICOM- \_ \_ Smartcard- \_ Benutzer \_ Speicher**, wird *StoreName* ignoriert. In diesem Fall liest CAPICOM alle Zertifikate aller verfügbaren Leser, die eine Smartcard enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Speicher**](store.md)
</dt> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**Schließen**](store-close.md)
</dt> </dl>

 

 
