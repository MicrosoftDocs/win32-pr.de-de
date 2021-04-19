---
description: Entschlüsselt den eingeschlossenen Inhalt.
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: EnvelopedData. entschlpt-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0c4c71ba0e3e0c2d421ad7bcbc9b1a61bb71d284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352979"
---
# <a name="envelopeddatadecrypt-method"></a><span data-ttu-id="3dc65-103">EnvelopedData. entschlpt-Methode</span><span class="sxs-lookup"><span data-stu-id="3dc65-103">EnvelopedData.Decrypt method</span></span>

<span data-ttu-id="3dc65-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3dc65-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3dc65-105">Verwenden Sie stattdessen die [**EnvelopedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="3dc65-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="3dc65-106">Mit  der Entschlüsselungsmethode werden eingeschlossene Inhalte entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="3dc65-106">The **Decrypt** method decrypts enveloped content.</span></span> <span data-ttu-id="3dc65-107">Die Entschlüsselung erfolgt, wenn der Empfänger der Nachricht Zugriff auf den [*privaten Schlüssel*](../secgloss/p-gly.md) hat, der mit einem der [*öffentlichen*](../secgloss/p-gly.md) Schlüssel gekoppelt ist, die zum Umhüllen der Nachricht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3dc65-107">Decryption is done if the recipient of the message has access to the [*private key*](../secgloss/p-gly.md) paired with one of the [*public keys*](../secgloss/p-gly.md) used to envelop the message.</span></span> <span data-ttu-id="3dc65-108">Durch Aufrufen der **Entschlüsselungsmethode** wird der [*Zustand*](../secgloss/s-gly.md) des-Objekts zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3dc65-108">Calling the **Decrypt** method resets the [*state*](../secgloss/s-gly.md) of the object.</span></span> <span data-ttu-id="3dc65-109">Wenn die **Entschlüsselungsmethode** erfolgreich ist, wird die [**Content**](envelopeddata-content.md) -Eigenschaft des [**EnvelopedData**](envelopeddata.md) -Objekts auf die Klartext-Nachricht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3dc65-109">If the **Decrypt** method succeeds, the [**Content**](envelopeddata-content.md) property of the [**EnvelopedData**](envelopeddata.md) object is set to the plaintext message.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dc65-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3dc65-110">Syntax</span></span>


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="3dc65-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dc65-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dc65-112">*Envelopedmessage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3dc65-112">*EnvelopedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dc65-113">Eine Zeichenfolge, die die zu entschlüsselnden Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="3dc65-113">String that contains the enveloped data to be decrypted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dc65-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3dc65-114">Return value</span></span>

<span data-ttu-id="3dc65-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3dc65-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dc65-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3dc65-116">Remarks</span></span>

<span data-ttu-id="3dc65-117">Die entschlüsselten Daten werden zu dem [**Content**](envelopeddata-content.md) -Eigenschafts Wert für das [**EnvelopedData**](envelopeddata.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3dc65-117">The decrypted data becomes the [**Content**](envelopeddata-content.md) property value for the [**EnvelopedData**](envelopeddata.md) object.</span></span>

<span data-ttu-id="3dc65-118">Wenn der Benutzer dieser Methode keinen Zugriff auf einen privaten Schlüssel hat, der mit einem der öffentlichen Schlüssel übereinstimmt, die zum Umhüllen der Nachricht verwendet werden, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="3dc65-118">If the user of this method does not have access to a private key that matches one of the public keys used to envelop the message, the method fails.</span></span> <span data-ttu-id="3dc65-119">Bei dieser Methode tritt ein Fehler auf, wenn sich das Zertifikat für den zugeordneten privaten Schlüssel weder auf dem lokalen Computer als auch auf dem Speicher des aktuellen Benutzers befindet.</span><span class="sxs-lookup"><span data-stu-id="3dc65-119">This method will fail if the certificate for the associated private key is not in either the local computer MY store or the current user MY store.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3dc65-120">Wenn diese Methode von einem Webskript aufgerufen wird, muss das Skript den [*privaten Schlüssel*](../secgloss/p-gly.md) verwenden, um die Daten zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="3dc65-120">When this method is called from a web script, the script needs to use your [*private key*](../secgloss/p-gly.md) to decrypt the data.</span></span> <span data-ttu-id="3dc65-121">Es ist ein Sicherheitsrisiko, nicht vertrauenswürdige Websites den privaten Schlüssel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3dc65-121">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="3dc65-122">Wenn diese Methode erstmals aufgerufen wird, wird ein Dialogfeld angezeigt, in dem Sie gefragt werden, ob die Website den privaten Schlüssel verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="3dc65-122">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="3dc65-123">Wenn Sie zulassen, dass das Skript den privaten Schlüssel verwendet, und wählen Sie "nicht mehr nachfragen", wird das Dialogfeld nicht mehr für Skripts angezeigt, die Ihren privaten Schlüssel zum Entschlüsseln von Daten in dieser Domäne verwenden.</span><span class="sxs-lookup"><span data-stu-id="3dc65-123">If you allow the script to use your private key and select "Do not ask me this again," the dialog box will no longer appear for any script that uses your private key to decrypt data within that domain.</span></span> <span data-ttu-id="3dc65-124">Skripts außerhalb dieser Domäne, die versuchen, den privaten Schlüssel zum Entschlüsseln von Daten zu verwenden, werden jedoch dennoch dazu führen, dass dieses Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3dc65-124">However, scripts outside that domain that attempt to use your private key to decrypt data will still cause this dialog box to appear.</span></span> <span data-ttu-id="3dc65-125">Wenn Sie dem Skript nicht gestatten, Ihren privaten Schlüssel zu verwenden, und die Option "Diese Meldung nicht mehr anzeigen" auswählen, wird die Möglichkeit der Verwendung Ihres privaten Schlüssels für das Entschlüsseln von Daten automatisch verweigert.</span><span class="sxs-lookup"><span data-stu-id="3dc65-125">If you do not allow the script to use your private key and select "Do not ask me this again," scripts within that domain will automatically be refused the ability to use your private key to decrypt data.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3dc65-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3dc65-126">Requirements</span></span>



| <span data-ttu-id="3dc65-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3dc65-127">Requirement</span></span> | <span data-ttu-id="3dc65-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3dc65-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dc65-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3dc65-129">End of client support</span></span><br/> | <span data-ttu-id="3dc65-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3dc65-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3dc65-131">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="3dc65-131">End of server support</span></span><br/> | <span data-ttu-id="3dc65-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3dc65-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3dc65-133">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="3dc65-133">Redistributable</span></span><br/>       | <span data-ttu-id="3dc65-134">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="3dc65-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3dc65-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3dc65-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3dc65-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dc65-136"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dc65-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dc65-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dc65-138">**Kryptografieobjekte**</span><span class="sxs-lookup"><span data-stu-id="3dc65-138">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="3dc65-139">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="3dc65-139">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
