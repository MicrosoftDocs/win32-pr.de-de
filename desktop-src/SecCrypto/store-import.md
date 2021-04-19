---
description: Die Import Methode kopiert den Inhalt eines zuvor exportierten Zertifikat Speicher in einen geöffneten Zertifikat Speicher. Diese Methode kann nur mit einem Speicher verwendet werden, der mit Lese-/Schreibberechtigung geöffnet wurde.
ms.assetid: 22db8f1c-469b-4baf-9039-4da35c9c6aa0
title: Store. Import-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4eb16cc341eb6e5dcee87216a52e9e3de94d1b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359712"
---
# <a name="storeimport-method"></a><span data-ttu-id="f7293-104">Store. Import-Methode</span><span class="sxs-lookup"><span data-stu-id="f7293-104">Store.Import method</span></span>

<span data-ttu-id="f7293-105">\[Die **Import** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f7293-105">\[The **Import** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f7293-106">Verwenden Sie stattdessen die [**X509Store-Klasse**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="f7293-106">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f7293-107">Die **Import** Methode kopiert den Inhalt eines zuvor exportierten Zertifikat Speicher in einen geöffneten [*Zertifikat Speicher*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f7293-107">The **Import** method copies into an open [*certificate store*](../secgloss/c-gly.md) the contents of a previously exported certificate store.</span></span> <span data-ttu-id="f7293-108">Diese Methode kann nur mit einem Speicher verwendet werden, der mit Lese-/Schreibberechtigung geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="f7293-108">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7293-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7293-109">Syntax</span></span>


```VB
Store.Import( _
  ByVal EncodedStore _
)
```



## <a name="parameters"></a><span data-ttu-id="f7293-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7293-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7293-111">*Encodstore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7293-111">*EncodedStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7293-112">Die Zeichenfolge, die die zu importierenden codierten Zertifikate enthält.</span><span class="sxs-lookup"><span data-stu-id="f7293-112">The string that contains the encoded certificates to be imported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7293-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7293-113">Return value</span></span>

<span data-ttu-id="f7293-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f7293-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7293-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7293-115">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7293-116">Wenn diese Methode von einem Webskript aufgerufen wird, muss das Skript auf die digitalen Zertifikate auf dem lokalen Computer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f7293-116">When this method is called from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="f7293-117">Wenn Sie zulassen, dass das Skript auf Ihre digitalen Zertifikate zugreift, erhält die Website, von der aus das Skript ausgeführt wird, auch Zugriff auf alle persönlichen Informationen, die in den Zertifikaten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f7293-117">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="f7293-118">Wenn diese Methode zum ersten Mal von einer bestimmten Domäne aufgerufen wird, wird ein Dialogfeld generiert, in dem der Benutzer angeben muss, ob der Zugriff auf die Zertifikate zulässig sein soll.</span><span class="sxs-lookup"><span data-stu-id="f7293-118">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span>

 

<span data-ttu-id="f7293-119">Wenn der Speicher nicht mit Lese-/Schreibberechtigungen geöffnet wird, schlägt diese Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="f7293-119">If the store is not opened with read/write permission, this method fails.</span></span> <span data-ttu-id="f7293-120">Obwohl diese Methode mit Speicher speichern verwendet werden kann, werden alle Änderungen, die an einem Speicher Speicher vorgenommen werden, beim Schließen des Speichers nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="f7293-120">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7293-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7293-121">Requirements</span></span>



| <span data-ttu-id="f7293-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7293-122">Requirement</span></span> | <span data-ttu-id="f7293-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f7293-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7293-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f7293-124">Redistributable</span></span><br/> | <span data-ttu-id="f7293-125">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="f7293-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f7293-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f7293-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="f7293-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7293-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7293-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7293-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7293-129">**Speicher**</span><span class="sxs-lookup"><span data-stu-id="f7293-129">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="f7293-130">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="f7293-130">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
