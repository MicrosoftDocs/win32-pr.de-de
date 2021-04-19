---
description: Die Remove-Methode entfernt ein Zertifikat aus einem geöffneten Zertifikat Speicher. Diese Methode kann nur mit einem Speicher verwendet werden, der mit Lese-/Schreibberechtigung geöffnet wurde.
ms.assetid: 02bb8ff1-2240-4ec7-b8af-9a7812a12ba9
title: Store. Remove-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 188553d6091314e1a872145219ea321d581b35c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368384"
---
# <a name="storeremove-method"></a><span data-ttu-id="220ea-104">Store. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="220ea-104">Store.Remove method</span></span>

<span data-ttu-id="220ea-105">\[Die **Remove** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="220ea-105">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="220ea-106">Verwenden Sie stattdessen die [**X509Store-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="220ea-106">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="220ea-107">Die **Remove** -Methode entfernt ein [*Zertifikat*](../secgloss/c-gly.md) aus einem geöffneten [*Zertifikat Speicher*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="220ea-107">The **Remove** method removes a [*certificate*](../secgloss/c-gly.md) from an open [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="220ea-108">Diese Methode kann nur mit einem Speicher verwendet werden, der mit Lese-/Schreibberechtigung geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="220ea-108">This method can only be used with a store that has been opened with read/write permission.</span></span>

## <a name="syntax"></a><span data-ttu-id="220ea-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="220ea-109">Syntax</span></span>


```VB
Store.Remove( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="220ea-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="220ea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="220ea-111">*Zertifikat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="220ea-111">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220ea-112">Ein Ausdruck, der zu einer Instanz eines [**Zertifikat**](certificate.md) Objekts aufgelöst wird, das aus dem Speicher entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="220ea-112">Expression that resolves to an instance of a [**Certificate**](certificate.md) object to be removed from the store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="220ea-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="220ea-113">Return value</span></span>

<span data-ttu-id="220ea-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="220ea-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="220ea-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="220ea-115">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="220ea-116">Wenn diese Methode von einem Webskript aufgerufen wird, muss das Skript digitale Zertifikate vom lokalen Computer löschen.</span><span class="sxs-lookup"><span data-stu-id="220ea-116">When this method is called from a web script, the script needs to delete digital certificates from the local computer.</span></span> <span data-ttu-id="220ea-117">Das Löschen digitaler Zertifikate durch nicht vertrauenswürdige Websites ist ein Sicherheitsrisiko.</span><span class="sxs-lookup"><span data-stu-id="220ea-117">Allowing untrusted websites to delete digital certificates is a security risk.</span></span> <span data-ttu-id="220ea-118">Ein Dialogfeld, in dem Sie gefragt werden, ob die Website Zertifikate löschen kann, wenn diese Methode zum ersten Mal aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="220ea-118">A dialog box that asks whether the website can delete certificates appears when this method is first called.</span></span> <span data-ttu-id="220ea-119">Wenn Sie der Anwendung das Löschen von Zertifikaten gestatten und dieses Dialogfeld nicht mehr anzeigen auswählen, wird das Dialogfeld nicht mehr für Skripts angezeigt, die Zertifikate innerhalb dieser Domäne löschen.</span><span class="sxs-lookup"><span data-stu-id="220ea-119">If you allow the application to delete certificates and select "Do not show this dialog box again," the dialog box will no longer appear for any script that deletes certificates within that domain.</span></span> <span data-ttu-id="220ea-120">Skripts außerhalb dieser Domäne, die versuchen, Zertifikate zu löschen, werden jedoch dennoch dazu führen, dass dieses Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="220ea-120">However, scripts outside that domain that attempt to delete certificates will still cause this dialog box to appear.</span></span> <span data-ttu-id="220ea-121">Wenn Sie das Skript nicht für das Löschen von Zertifikaten zulassen und das Kontrollkästchen Dieses Dialogfeld nicht mehr anzeigen aktivieren, wird das Löschen von Zertifikaten automatisch verweigert.</span><span class="sxs-lookup"><span data-stu-id="220ea-121">If you do not allow the script to delete certificates and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to delete certificates.</span></span>

 

<span data-ttu-id="220ea-122">Wenn Sie ein Zertifikat aus einem Speicher löschen, sollten Sie zuerst den dem Zertifikat zugeordneten privaten Schlüssel löschen.</span><span class="sxs-lookup"><span data-stu-id="220ea-122">When you delete a certificate from a store, you should first delete the private key associated with the certificate.</span></span>

<span data-ttu-id="220ea-123">Wenn der Speicher nicht mit Lese-/Schreibberechtigungen geöffnet ist, schlägt diese Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="220ea-123">If the store is not open with read/write permission, this method fails.</span></span> <span data-ttu-id="220ea-124">Obwohl diese Methode mit Speicher speichern verwendet werden kann, werden alle Änderungen, die an einem Speicher Speicher vorgenommen werden, beim Schließen des Speichers nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="220ea-124">Although this method can be used with memory stores, any changes made to a memory store are not persisted when the store is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="220ea-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="220ea-125">Requirements</span></span>



| <span data-ttu-id="220ea-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="220ea-126">Requirement</span></span> | <span data-ttu-id="220ea-127">Wert</span><span class="sxs-lookup"><span data-stu-id="220ea-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="220ea-128">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="220ea-128">Redistributable</span></span><br/> | <span data-ttu-id="220ea-129">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="220ea-129">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="220ea-130">DLL</span><span class="sxs-lookup"><span data-stu-id="220ea-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="220ea-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="220ea-131"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="220ea-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="220ea-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="220ea-133">**Speicher**</span><span class="sxs-lookup"><span data-stu-id="220ea-133">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="220ea-134">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="220ea-134">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
