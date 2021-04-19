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
# <a name="storeopen-method"></a><span data-ttu-id="e0842-103">Store. Open-Methode</span><span class="sxs-lookup"><span data-stu-id="e0842-103">Store.Open method</span></span>

<span data-ttu-id="e0842-104">\[Die **Open** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e0842-104">\[The **Open** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e0842-105">Verwenden Sie stattdessen die [**X509Store-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="e0842-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e0842-106">Die **Open** -Methode öffnet einen angegebenen [*Zertifikat Speicher*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e0842-106">The **Open** method opens a specified [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="e0842-107">Standardmäßig werden der Speicherort für den aktuellen CAPICOM \_ \_ \_ -Benutzer Speicherort und der CAPICOM- \_ \_ Speicher für mein Geschäft als schreibgeschützt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e0842-107">By default, the CAPICOM\_CURRENT\_USER\_STORE location and CAPICOM\_MY\_STORE store are opened as read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0842-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0842-108">Syntax</span></span>


```VB
Store.Open( _
  [ ByVal StoreLocation ], _
  [ ByVal StoreName ], _
  [ ByVal OpenMode ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e0842-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0842-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0842-110">*Storeloation* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e0842-110">*StoreLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0842-111">Ein Wert der [CAPICOM \_ Store \_ Location](capicom-store-location.md) -Enumeration, der den Speicherort des zu öffnenden Stores angibt.</span><span class="sxs-lookup"><span data-stu-id="e0842-111">A value of the [CAPICOM\_STORE\_LOCATION](capicom-store-location.md) enumeration that indicates the location of the store to be opened.</span></span> <span data-ttu-id="e0842-112">Der Standardwert ist "CAPICOM \_ Current \_ User \_ Store".</span><span class="sxs-lookup"><span data-stu-id="e0842-112">The default value is CAPICOM\_CURRENT\_USER\_STORE.</span></span> <span data-ttu-id="e0842-113">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="e0842-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e0842-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e0842-114">Value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="e0842-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e0842-115">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <span data-ttu-id="e0842-116"><dt>**CAPICOM \_ Active \_ Directory- \_ Benutzer \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="e0842-116"><dt>**CAPICOM\_ACTIVE\_DIRECTORY\_USER\_STORE**</dt></span></span> </dl> | <span data-ttu-id="e0842-117">Der Speicher ist ein Active Directory Speicher.</span><span class="sxs-lookup"><span data-stu-id="e0842-117">The store is an Active Directory store.</span></span> <span data-ttu-id="e0842-118">Wenn ein Active Directory Speicher als Lese-/Schreibzugriff geöffnet ist, wird kein Fehler generiert, aber alle Änderungen am Speicher werden nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e0842-118">No error will be generated if an Active Directory store is opened as read/write, but any changes to the store will not be persisted.</span></span> <span data-ttu-id="e0842-119">Zertifikate können Active Directory speichern nicht hinzugefügt oder daraus entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e0842-119">Certificates cannot be added to or removed from Active Directory stores.</span></span><br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <span data-ttu-id="e0842-120"><dt>**CAPICOM \_ aktueller \_ Benutzer \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="e0842-120"><dt>**CAPICOM\_CURRENT\_USER\_STORE**</dt></span></span> </dl>                             | <span data-ttu-id="e0842-121">Der Speicher ist ein aktueller Benutzerspeicher.</span><span class="sxs-lookup"><span data-stu-id="e0842-121">The store is a current user store.</span></span> <span data-ttu-id="e0842-122">Ein aktueller Benutzerspeicher kann ein Lese-/Schreibspeicher sein.</span><span class="sxs-lookup"><span data-stu-id="e0842-122">A current user store may be a read/write store.</span></span> <span data-ttu-id="e0842-123">Wenn dies der Fall ist, werden Änderungen am Inhalt des Stores persistent gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e0842-123">If it is, changes in the contents of the store are persisted.</span></span><br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <span data-ttu-id="e0842-124"><dt>**lokaler CAPICOM- \_ \_ Computer \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="e0842-124"><dt>**CAPICOM\_LOCAL\_MACHINE\_STORE**</dt></span></span> </dl>                          | <span data-ttu-id="e0842-125">Der Speicher ist ein lokaler Computerspeicher.</span><span class="sxs-lookup"><span data-stu-id="e0842-125">The store is a local computer store.</span></span> <span data-ttu-id="e0842-126">Lokale Computerspeicher können nur Lese-/Schreibspeicher sein, wenn der Benutzer über Lese-/Schreibberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="e0842-126">Local computer stores can be read/write stores only if the user has read/write permissions.</span></span> <span data-ttu-id="e0842-127">Wenn der Benutzer über Lese-/Schreibberechtigungen verfügt und der Speicher mit Lese-/Schreibzugriff geöffnet wird, werden Änderungen im Inhalt des Stores beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e0842-127">If the user has read/write permissions and if the store is opened read/write, then changes in the contents of the store are persisted.</span></span><br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <span data-ttu-id="e0842-128"><dt>**CAPICOM- \_ Speicher Speicher \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0842-128"><dt>**CAPICOM\_MEMORY\_STORE**</dt></span></span> </dl>                                                | <span data-ttu-id="e0842-129">Der Speicher ist ein Speicher Speicher.</span><span class="sxs-lookup"><span data-stu-id="e0842-129">The store is a memory store.</span></span> <span data-ttu-id="e0842-130">Alle Änderungen im Inhalt des Stores werden nicht persistent gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e0842-130">Any changes in the contents of the store are not persisted.</span></span><br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <span data-ttu-id="e0842-131"><dt>**CAPICOM \_ - \_ Smartcard- \_ Benutzer \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="e0842-131"><dt>**CAPICOM\_SMART\_CARD\_USER\_STORE**</dt></span></span> </dl>                   | <span data-ttu-id="e0842-132">Der Speicher ist die Gruppe der vorhandenen Smartcards.</span><span class="sxs-lookup"><span data-stu-id="e0842-132">The store is the group of present smart cards.</span></span> <span data-ttu-id="e0842-133">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e0842-133">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="e0842-134">*StoreName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e0842-134">*StoreName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0842-135">Eine Zeichenfolge, die den Namen des zu öffnenden Systemzertifikat Speicher enthält.</span><span class="sxs-lookup"><span data-stu-id="e0842-135">A string that contains the name of the system certificate store to be opened.</span></span> <span data-ttu-id="e0842-136">Der Standardwert ist "CAPICOM \_ My \_ Store".</span><span class="sxs-lookup"><span data-stu-id="e0842-136">The default value is CAPICOM\_MY\_STORE.</span></span> <span data-ttu-id="e0842-137">Wenn der Speicher von einem Webskript aus geöffnet wird, ist der umgekehrte Schrägstrich ( \\ ) im Namen nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="e0842-137">If the store is opened from a web script, the backslash (\\) character is not allowed in the name.</span></span> <span data-ttu-id="e0842-138">Zusätzlich zu den durch das System definierten speichern können benutzerdefinierte Speicher geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="e0842-138">In addition to stores defined by the system, user-defined stores can be opened.</span></span>

<span data-ttu-id="e0842-139">Dieser Parameter kann ein benutzerdefinierter Speicher oder einer der folgenden Systemzertifikat Speicher sein.</span><span class="sxs-lookup"><span data-stu-id="e0842-139">This parameter can be a user-defined store or one of the following system certificate stores.</span></span>



| <span data-ttu-id="e0842-140">Wert</span><span class="sxs-lookup"><span data-stu-id="e0842-140">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="e0842-141">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e0842-141">Meaning</span></span>                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <span data-ttu-id="e0842-142"><dt>**CAPICOM- \_ ca- \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="e0842-142"><dt>**CAPICOM\_CA\_STORE**</dt></span></span> </dl>          | <span data-ttu-id="e0842-143">CA-Speicher.</span><span class="sxs-lookup"><span data-stu-id="e0842-143">CA store.</span></span> <span data-ttu-id="e0842-144">Dieser Speicher wird zum Speichern von zwischen Zertifizierungsstellen-Zertifikaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0842-144">This store is used to store intermediate CA certificates.</span></span><br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <span data-ttu-id="e0842-145"><dt>**CAPICOM \_ mein \_ Geschäft**</dt></span><span class="sxs-lookup"><span data-stu-id="e0842-145"><dt>**CAPICOM\_MY\_STORE**</dt></span></span> </dl>          | <span data-ttu-id="e0842-146">Mein Geschäft.</span><span class="sxs-lookup"><span data-stu-id="e0842-146">My store.</span></span> <span data-ttu-id="e0842-147">Dieser Speicher wird für die persönlichen Zertifikate eines Benutzers verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0842-147">This store is used for a user's personal certificates.</span></span><br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <span data-ttu-id="e0842-148"><dt>**CAPICOM \_ anderer \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="e0842-148"><dt>**CAPICOM\_OTHER\_STORE**</dt></span></span> </dl> | <span data-ttu-id="e0842-149">Addressbook-Speicher.</span><span class="sxs-lookup"><span data-stu-id="e0842-149">AddressBook store.</span></span> <span data-ttu-id="e0842-150">Dieser Speicher wird verwendet, um die Zertifikate anderer Benutzer beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="e0842-150">This store is used to keep the certificates of others.</span></span><br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <span data-ttu-id="e0842-151"><dt>**CAPICOM-Stamm \_ \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="e0842-151"><dt>**CAPICOM\_ROOT\_STORE**</dt></span></span> </dl>    | <span data-ttu-id="e0842-152">Stamm Speicher.</span><span class="sxs-lookup"><span data-stu-id="e0842-152">Root store.</span></span> <span data-ttu-id="e0842-153">Dieser Speicher wird verwendet, um die Stamm Zertifizierungsstelle und selbst signierte vertrauenswürdige Zertifikate zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e0842-153">This store is used to store the root CA and self-signed, trusted certificates.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e0842-154">*OpenMode* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e0842-154">*OpenMode* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0842-155">Ein Wert der-Enumeration des [CAPICOM- \_ Speicher \_ öffnenden \_ Modus](capicom-store-open-mode.md) , der den Öffnungs Modus des Stores angibt.</span><span class="sxs-lookup"><span data-stu-id="e0842-155">A value of the [CAPICOM\_STORE\_OPEN\_MODE](capicom-store-open-mode.md) enumeration that indicates the open mode of the store.</span></span> <span data-ttu-id="e0842-156">Der Standardwert ist "CAPICOM \_ Store \_ Open \_ Read \_ only".</span><span class="sxs-lookup"><span data-stu-id="e0842-156">The default value is CAPICOM\_STORE\_OPEN\_READ\_ONLY.</span></span> <span data-ttu-id="e0842-157">Wenn der Speicher von einem Webskript aus geöffnet wird, wird dieser Wert erzwungen, dass der CAPICOM- \_ Speicher \_ nur geöffnet ist \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e0842-157">If the store is opened from a web script, this value is forced to CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY.</span></span> <span data-ttu-id="e0842-158">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="e0842-158">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e0842-159">Wert</span><span class="sxs-lookup"><span data-stu-id="e0842-159">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="e0842-160">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e0842-160">Meaning</span></span>                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <span data-ttu-id="e0842-161"><dt>**\_ \_ \_ maximal zulässige Anzahl geöffneter CAPICOM-Speicher \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0842-161"><dt>**CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED**</dt></span></span> </dl> | <span data-ttu-id="e0842-162">Öffnen Sie den Speicher im Lese-/Schreibmodus, wenn der Benutzer über Lese-/Schreibberechtigungen verfügt. Andernfalls öffnen Sie den Speicher im schreibgeschützten Modus.</span><span class="sxs-lookup"><span data-stu-id="e0842-162">Open the store in read/write mode if the user has read/write permissions; otherwise, open the store in read-only mode.</span></span><br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <span data-ttu-id="e0842-163"><dt>**CAPICOM \_ Store \_ Open \_ Read \_ Only**</dt></span><span class="sxs-lookup"><span data-stu-id="e0842-163"><dt>**CAPICOM\_STORE\_OPEN\_READ\_ONLY**</dt></span></span> </dl>                   | <span data-ttu-id="e0842-164">Öffnen Sie den Speicher im schreibgeschützten Modus.</span><span class="sxs-lookup"><span data-stu-id="e0842-164">Open the store in read-only mode.</span></span><br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <span data-ttu-id="e0842-165"><dt>**CAPICOM \_ Store \_ offene \_ Lese- \_ /Schreibzugriff**</dt></span><span class="sxs-lookup"><span data-stu-id="e0842-165"><dt>**CAPICOM\_STORE\_OPEN\_READ\_WRITE**</dt></span></span> </dl>                | <span data-ttu-id="e0842-166">Öffnen Sie den Speicher im Lese-/Schreibmodus.</span><span class="sxs-lookup"><span data-stu-id="e0842-166">Open the store in read/write mode.</span></span><br/>                                                                                     |



 

<span data-ttu-id="e0842-167">Die folgenden Flags können mit den Werten in der vorherigen Tabelle mithilfe einer logischen **or** -Operation kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="e0842-167">The following flags can be combined with the values in the previous table by using a logical-**OR** operation.</span></span>



| <span data-ttu-id="e0842-168">Wert</span><span class="sxs-lookup"><span data-stu-id="e0842-168">Value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="e0842-169">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e0842-169">Meaning</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <span data-ttu-id="e0842-170"><dt>**CAPICOM \_ - \_ Speicher \_ Öffnen \_ nur vorhanden**</dt></span><span class="sxs-lookup"><span data-stu-id="e0842-170"><dt>**CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY**</dt></span></span> </dl>          | <span data-ttu-id="e0842-171">Nur vorhandene Speicher öffnen; Erstellen Sie keinen neuen Speicher.</span><span class="sxs-lookup"><span data-stu-id="e0842-171">Open existing stores only; do not create a new store.</span></span> <span data-ttu-id="e0842-172">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e0842-172">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <span data-ttu-id="e0842-173"><dt>**CAPICOM \_ Store \_ Open \_ include \_ archiviert**</dt></span><span class="sxs-lookup"><span data-stu-id="e0842-173"><dt>**CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED**</dt></span></span> </dl> | <span data-ttu-id="e0842-174">Schließt Archivierte Zertifikate ein, wenn der Speicher verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e0842-174">Include archived certificates when using the store.</span></span> <span data-ttu-id="e0842-175">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e0842-175">Introduced in CAPICOM 2.0.</span></span><br/>   |



 

<span data-ttu-id="e0842-176">Filialen an manchen Speicherorten können nur im schreibgeschützten Modus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="e0842-176">Stores in some locations can be opened only in read-only mode.</span></span> <span data-ttu-id="e0842-177">Hierzu gehören alle Filialen im lokalen CAPICOM- \_ \_ Computer \_ Speicher, für die der Benutzer nicht über Schreibberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="e0842-177">These include all stores in CAPICOM\_LOCAL\_MACHINE\_STORE for which the user does not have write permissions.</span></span> <span data-ttu-id="e0842-178">Wenn versucht wird, einen Speicher ohne angemessenen Zugriff als Lese-/Schreibspeicher zu öffnen, führt dies zu einem Fehler bei der **Open** -Methode.</span><span class="sxs-lookup"><span data-stu-id="e0842-178">Attempts to open a store as a read/write store without proper access and permissions will result in the failure of the **Open** method.</span></span> <span data-ttu-id="e0842-179">Active Directory Stores können als Lese-/Schreibspeicher geöffnet werden, ohne dass die **Open** -Methode ausfällt, Änderungen am Speicher werden jedoch nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e0842-179">Active Directory stores can be opened as a read/write store without failure of the **Open** method, but changes to the store will not be persisted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0842-180">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0842-180">Return value</span></span>

<span data-ttu-id="e0842-181">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e0842-181">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0842-182">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0842-182">Remarks</span></span>

<span data-ttu-id="e0842-183">Wenn diese Methode in einem smartcardspeicher aufgerufen wird, können zusätzliche Smartcard-Benutzeroberflächen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e0842-183">If this method is called on a SmartCard store, additional SmartCard user interfaces may be invoked.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0842-184">Wenn diese Methode von einem Webskript aufgerufen wird, muss das Skript auf die digitalen Zertifikate auf dem lokalen Computer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e0842-184">When this method is called from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="e0842-185">Wenn Sie zulassen, dass das Skript auf Ihre digitalen Zertifikate zugreift, erhält die Website, von der aus das Skript ausgeführt wird, auch Zugriff auf alle persönlichen Informationen, die in den Zertifikaten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e0842-185">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="e0842-186">Wenn diese Methode zum ersten Mal von einer bestimmten Domäne aufgerufen wird, wird ein Dialogfeld generiert, in dem der Benutzer angeben muss, ob der Zugriff auf die Zertifikate zulässig sein soll.</span><span class="sxs-lookup"><span data-stu-id="e0842-186">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span> <span data-ttu-id="e0842-187">Speicher, die von einem Webskript geöffnet wurden, erzwingen automatisch, dass das CAPICOM- \_ Speicher-Flag " \_ \_ vorhandenes \_</span><span class="sxs-lookup"><span data-stu-id="e0842-187">Stores opened from a web script automatically force the CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY flag.</span></span>

 

<span data-ttu-id="e0842-188">Handelt es sich bei *storeloation* um **CAPICOM- \_ \_ Smartcard- \_ Benutzer \_ Speicher**, wird *StoreName* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e0842-188">If *StoreLocation* is **CAPICOM\_SMART\_CARD\_USER\_STORE**, *StoreName* is ignored.</span></span> <span data-ttu-id="e0842-189">In diesem Fall liest CAPICOM alle Zertifikate aller verfügbaren Leser, die eine Smartcard enthalten.</span><span class="sxs-lookup"><span data-stu-id="e0842-189">In this case, CAPICOM reads all certificates from all available readers that contain a smart card.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0842-190">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0842-190">Requirements</span></span>



| <span data-ttu-id="e0842-191">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0842-191">Requirement</span></span> | <span data-ttu-id="e0842-192">Wert</span><span class="sxs-lookup"><span data-stu-id="e0842-192">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0842-193">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e0842-193">Redistributable</span></span><br/> | <span data-ttu-id="e0842-194">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="e0842-194">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e0842-195">DLL</span><span class="sxs-lookup"><span data-stu-id="e0842-195">DLL</span></span><br/>             | <dl> <span data-ttu-id="e0842-196"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0842-196"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0842-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0842-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0842-198">**Speicher**</span><span class="sxs-lookup"><span data-stu-id="e0842-198">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="e0842-199">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="e0842-199">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="e0842-200">**Schließen**</span><span class="sxs-lookup"><span data-stu-id="e0842-200">**Close**</span></span>](store-close.md)
</dt> </dl>

 

 
