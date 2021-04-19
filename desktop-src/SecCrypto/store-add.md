---
description: Fügt einem geöffneten Zertifikat Speicher ein Zertifikat Objekt hinzu.
ms.assetid: 787b8a41-dcdb-4b5b-a1fd-f5424300361b
title: Store. Add-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d217c784fa5f994e88ee2de78f2e1944091d724
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365682"
---
# <a name="storeadd-method"></a><span data-ttu-id="0269c-103">Store. Add-Methode</span><span class="sxs-lookup"><span data-stu-id="0269c-103">Store.Add method</span></span>

<span data-ttu-id="0269c-104">\[Die **Add** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="0269c-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0269c-105">Verwenden Sie stattdessen die [**X509Store-Klasse**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="0269c-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0269c-106">Mit der **Add** -Methode wird einem geöffneten [*Zertifikat Speicher*](../secgloss/c-gly.md)ein [**Zertifikat**](certificate.md) Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0269c-106">The **Add** method adds a [**Certificate**](certificate.md) object to an open [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="0269c-107">Diese Methode kann nur mit einem Speicher verwendet werden, der mit Lese-/Schreibberechtigung geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="0269c-107">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="0269c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0269c-108">Syntax</span></span>


```VB
Store.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="0269c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0269c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0269c-110">*Zertifikat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0269c-110">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0269c-111">Ein Ausdruck, der zu einem [**Zertifikat**](certificate.md) Objekt aufgelöst wird, das dem Speicher hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0269c-111">Expression that resolves to a [**Certificate**](certificate.md) object to be added to the store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0269c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0269c-112">Return value</span></span>

<span data-ttu-id="0269c-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0269c-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0269c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0269c-114">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0269c-115">Wenn diese Methode von einem Webskript in einem Systemspeicher aufgerufen wird, muss das Skript auf die digitalen Zertifikate auf dem lokalen Computer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="0269c-115">When this method is called on a system store from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="0269c-116">Wenn Sie zulassen, dass das Skript auf Ihre digitalen Zertifikate zugreift, erhält die Website, von der aus das Skript ausgeführt wird, auch Zugriff auf alle persönlichen Informationen, die in den Zertifikaten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="0269c-116">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="0269c-117">Wenn diese Methode zum ersten Mal von einer bestimmten Domäne aufgerufen wird, wird ein Dialogfeld generiert, in dem der Benutzer angeben muss, ob der Zugriff auf die Zertifikate zulässig sein soll.</span><span class="sxs-lookup"><span data-stu-id="0269c-117">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span>

 

<span data-ttu-id="0269c-118">Wenn der Speicher nicht im Lese-/Schreibmodus geöffnet ist, schlägt diese Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="0269c-118">If the store is not open in read/write mode, this method fails.</span></span> <span data-ttu-id="0269c-119">Obwohl diese Methode mit Speicher speichern verwendet werden kann, werden alle Änderungen, die an einem Speicher Speicher vorgenommen werden, beim Schließen des Speichers nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="0269c-119">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

<span data-ttu-id="0269c-120">Wenn das Zertifikat, das dem Speicher hinzugefügt wird, identisch mit dem Zertifikat ist, das bereits vorhanden ist, löscht die **Add** -Methode das vorhandene Zertifikat aus dem Speicher und fügt dann das neue Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="0269c-120">If the certificate being added to the store is the same as one that is already there, the **Add** method deletes the existing certificate from the store and then adds the new certificate.</span></span> <span data-ttu-id="0269c-121">Das neue Zertifikat erbt die Eigenschaften des vorhandenen Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="0269c-121">The new certificate inherits properties from the existing certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="0269c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0269c-122">Requirements</span></span>



| <span data-ttu-id="0269c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0269c-123">Requirement</span></span> | <span data-ttu-id="0269c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0269c-124">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0269c-125">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="0269c-125">Redistributable</span></span><br/> | <span data-ttu-id="0269c-126">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="0269c-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0269c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0269c-127">DLL</span></span><br/>             | <dl> <span data-ttu-id="0269c-128"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0269c-128"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0269c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0269c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0269c-130">**Speicher**</span><span class="sxs-lookup"><span data-stu-id="0269c-130">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="0269c-131">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="0269c-131">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
