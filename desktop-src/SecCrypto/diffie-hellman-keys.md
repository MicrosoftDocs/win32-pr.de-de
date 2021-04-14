---
description: Erläutert, wie Diffie-Hellman Schlüssel generiert, ausgetauscht, importiert und exportiert werden.
ms.assetid: 623a8c9e-3f6a-470b-be30-dec13342bb90
title: Diffie-Hellman Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00eaddd580ac74e18e26498175f87b5d81b8e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350148"
---
# <a name="diffie-hellman-keys"></a><span data-ttu-id="e54cb-103">Diffie-Hellman Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e54cb-103">Diffie-Hellman Keys</span></span>

-   [<span data-ttu-id="e54cb-104">Erstellen von Diffie-Hellman Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="e54cb-104">Generating Diffie-Hellman Keys</span></span>](#generating-diffie-hellman-keys)
-   [<span data-ttu-id="e54cb-105">Austauschen von Diffie-Hellman Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="e54cb-105">Exchanging Diffie-Hellman Keys</span></span>](#exchanging-diffie-hellman-keys)
-   [<span data-ttu-id="e54cb-106">Exportieren eines Diffie-Hellman privaten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="e54cb-106">Exporting a Diffie-Hellman Private Key</span></span>](#exporting-a-diffie-hellman-private-key)
-   [<span data-ttu-id="e54cb-107">Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="e54cb-107">Example Code</span></span>](#example-code)

## <a name="generating-diffie-hellman-keys"></a><span data-ttu-id="e54cb-108">Erstellen von Diffie-Hellman Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="e54cb-108">Generating Diffie-Hellman Keys</span></span>

<span data-ttu-id="e54cb-109">Führen Sie die folgenden Schritte aus, um einen Diffie-Hellman Schlüssel zu generieren:</span><span class="sxs-lookup"><span data-stu-id="e54cb-109">To generate a Diffie-Hellman key, perform the following steps:</span></span>

1.  <span data-ttu-id="e54cb-110">Aufrufen der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion, um ein Handle für den Kryptografieanbieter von Microsoft Diffie-Hellman zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e54cb-110">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="e54cb-111">Generieren Sie den neuen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="e54cb-111">Generate the new key.</span></span> <span data-ttu-id="e54cb-112">Es gibt zwei Möglichkeiten, diesen – zu erreichen, indem CryptoAPI alle neuen Werte für g, P und X generiert, oder wenn vorhandene Werte für g und P verwendet werden und ein neuer Wert für X generiert wird.</span><span class="sxs-lookup"><span data-stu-id="e54cb-112">There are two ways to accomplish this—by having CryptoAPI generate all new values for G, P, and X or by using existing values for G and P, and generating a new value for X.</span></span>

    <span data-ttu-id="e54cb-113">**So generieren Sie den Schlüssel, indem Sie alle neuen Werte generieren**</span><span class="sxs-lookup"><span data-stu-id="e54cb-113">**To generate the key by generating all new values**</span></span>

    1.  <span data-ttu-id="e54cb-114">Aufrufen der [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) -Funktion, wobei entweder **calg \_ dh \_ SF** (speichern und Weiterleiten) oder **calg \_ dh \_ ephem** (kurzlebige) im *algid* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e54cb-114">Call the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function, passing either **CALG\_DH\_SF** (store and forward) or **CALG\_DH\_EPHEM** (ephemeral) in the *Algid* parameter.</span></span> <span data-ttu-id="e54cb-115">Der Schlüssel wird mithilfe neuer, zufälliger Werte für G und P generiert, ein neu berechneter Wert für X, und sein Handle wird im *phkey* -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e54cb-115">The key will be generated using new, random values for G and P, a newly calculated value for X, and its handle will be returned in the *phKey* parameter.</span></span>
    2.  <span data-ttu-id="e54cb-116">Der neue Schlüssel ist jetzt einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="e54cb-116">The new key is now ready for use.</span></span> <span data-ttu-id="e54cb-117">Die Werte von G und P müssen bei einem [*Schlüsselaustausch*](../secgloss/e-gly.md)zusammen mit dem Schlüssel an den Empfänger gesendet werden (oder von einer anderen Methode gesendet werden).</span><span class="sxs-lookup"><span data-stu-id="e54cb-117">The values of G and P must be sent to the recipient along with the key (or sent by some other method) when doing a [*key exchange*](../secgloss/e-gly.md).</span></span>

    <span data-ttu-id="e54cb-118">**So generieren Sie den Schlüssel mithilfe vordefinierter Werte für G und P**</span><span class="sxs-lookup"><span data-stu-id="e54cb-118">**To generate the key by using predefined values for G and P**</span></span>

    1.  <span data-ttu-id="e54cb-119">Rufen Sie [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) auf, indem Sie entweder **calg \_ dh \_ SF** (speichern und Weiterleiten) oder **calg \_ dh \_ ephem** (kurzlebige) im *algid* -Parameter und **crypt \_ pregen** für den *dwFlags* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="e54cb-119">Call [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) passing either **CALG\_DH\_SF** (store and forward) or **CALG\_DH\_EPHEM** (ephemeral) in the *Algid* parameter and **CRYPT\_PREGEN** for the *dwFlags* parameter.</span></span> <span data-ttu-id="e54cb-120">Ein Schlüssel Handle wird generiert und im *phkey* -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e54cb-120">A key handle will be generated and returned in the *phKey* parameter.</span></span>
    2.  <span data-ttu-id="e54cb-121">Initialisieren Sie eine [**crypt \_ Data \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) -Struktur mit dem **pbData** -Member, der auf den P-Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e54cb-121">Initialize a [**CRYPT\_DATA\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure with the **pbData** member set to the P value.</span></span> <span data-ttu-id="e54cb-122">Das [*BLOB*](../secgloss/b-gly.md) enthält keine Header Informationen, und der **pbData** -Member weist das [*Little-Endian-*](../secgloss/l-gly.md) Format auf.</span><span class="sxs-lookup"><span data-stu-id="e54cb-122">The [*BLOB*](../secgloss/b-gly.md) contains no header information and the **pbData** member is in [*little-endian*](../secgloss/l-gly.md) format.</span></span>
    3.  <span data-ttu-id="e54cb-123">Der Wert von P wird durch Aufrufen der [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) -Funktion festgelegt, wobei das in Schritt a abgerufene Schlüssel Handle im *HKEY* -Parameter, das **KP- \_ P** -Flag im *dwparam* -Parameter und ein Zeiger auf die-Struktur mit dem Wert P im *pbData* -Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e54cb-123">The value of P is set by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_P** flag in the *dwParam* parameter, and a pointer to the structure that contains the value of P in the *pbData* parameter.</span></span>
    4.  <span data-ttu-id="e54cb-124">Initialisieren Sie eine [**crypt \_ Data \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) -Struktur mit dem **pbData** -Member, der auf den Wert G festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e54cb-124">Initialize a [**CRYPT\_DATA\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure with the **pbData** member set to the G value.</span></span> <span data-ttu-id="e54cb-125">Das BLOB enthält keine Header Informationen, und der **pbData** -Member weist das Little-Endian-Format auf.</span><span class="sxs-lookup"><span data-stu-id="e54cb-125">The BLOB contains no header information and the **pbData** member is in little-endian format.</span></span>
    5.  <span data-ttu-id="e54cb-126">Der Wert von "G" wird durch Aufrufen der Funktion " [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) " festgelegt, wobei das in Schritt a abgerufene Schlüssel Handle im *HKEY* -Parameter, das **KP \_ G** -Flag im *dwparam* -Parameter und ein Zeiger auf die Struktur mit dem Wert "G" im *pbData* -Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e54cb-126">The value of G is set by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_G** flag in the *dwParam* parameter, and a pointer to the structure that contains the value of G in the *pbData* parameter.</span></span>
    6.  <span data-ttu-id="e54cb-127">Der Wert von "X" wird durch Aufrufen der Funktion " [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) " generiert, wobei das in Schritt a abgerufene Schlüssel Handle im *HKEY* -Parameter, das **KP \_ X** -Flag im *dwparam* -Parameter und **null** im *pbData* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e54cb-127">The value of X is generated by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_X** flag in the *dwParam* parameter, and **NULL** in the *pbData* parameter.</span></span>
    7.  <span data-ttu-id="e54cb-128">Wenn alle Funktionsaufrufe erfolgreich waren, ist der Diffie-Hellman öffentliche Schlüssel einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="e54cb-128">If all the function calls succeeded, the Diffie-Hellman public key is ready for use.</span></span>

3.  <span data-ttu-id="e54cb-129">Wenn der Schlüssel nicht mehr benötigt wird, zerstören Sie ihn, indem Sie das Schlüssel Handle an die [**cryptdestroykey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) -Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="e54cb-129">When the key is no longer needed, destroy it by passing the key handle to the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function.</span></span>

<span data-ttu-id="e54cb-130">Wenn **calg \_ dh \_ SF** in den vorherigen Prozeduren angegeben wurde, werden die Schlüsselwerte im Speicher gespeichert, wobei jeder Rückruf von [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e54cb-130">If **CALG\_DH\_SF** was specified in the previous procedures, the key values are persisted to storage with each call to [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span></span> <span data-ttu-id="e54cb-131">Die Werte G und P können dann mithilfe der [**cryptgetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) -Funktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e54cb-131">The G and P values can then be retrieved by using the [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) function.</span></span> <span data-ttu-id="e54cb-132">Einige CSPs verfügen möglicherweise über hart codierte G-und P-Werte.</span><span class="sxs-lookup"><span data-stu-id="e54cb-132">Some CSPs may have hard-coded G and P values.</span></span> <span data-ttu-id="e54cb-133">In diesem Fall wird ein ". **\_ fixedparameter** "-Fehler zurückgegeben, wenn **cryptsetkeyparam** mit **KP \_ G** oder **KP \_ P** aufgerufen wird, das im *dwparam* -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e54cb-133">In this case a **NTE\_FIXEDPARAMETER** error will be returned if **CryptSetKeyParam** is called with **KP\_G** or **KP\_P** specified in the *dwParam* parameter.</span></span> <span data-ttu-id="e54cb-134">Wenn **cryptdestroykey** aufgerufen wird, wird das Handle für den Schlüssel zerstört, aber die Schlüsselwerte werden im CSP beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e54cb-134">If **CryptDestroyKey** is called, the handle to the key is destroyed, but the key values are retained in the CSP.</span></span> <span data-ttu-id="e54cb-135">Wenn jedoch **calg \_ dh \_ ephem** angegeben wurde, wird das Handle für den Schlüssel zerstört, und alle Werte werden vom CSP gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e54cb-135">However, if **CALG\_DH\_EPHEM** was specified, the handle to the key is destroyed, and all values are cleared from the CSP.</span></span>

## <a name="exchanging-diffie-hellman-keys"></a><span data-ttu-id="e54cb-136">Austauschen von Diffie-Hellman Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="e54cb-136">Exchanging Diffie-Hellman Keys</span></span>

<span data-ttu-id="e54cb-137">Der Zweck des Diffie-Hellman Algorithmus besteht darin, dass zwei oder mehr Parteien einen identischen geheimen Sitzungsschlüssel erstellen und freigeben können, indem Informationen über ein nicht sicheres Netzwerk freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e54cb-137">The purpose of the Diffie-Hellman algorithm is to make it possible for two or more parties to create and share an identical, secret session key by sharing information over a network that is not secure.</span></span> <span data-ttu-id="e54cb-138">Die Informationen, die über das Netzwerk freigegeben werden, sind in Form von einigen Konstanten Werten und einem Diffie-Hellman öffentlichen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="e54cb-138">The information that gets shared over the network is in the form of a couple of constant values and a Diffie-Hellman public key.</span></span> <span data-ttu-id="e54cb-139">Der Prozess, der von zwei Schlüsselaustausch Parteien verwendet wird, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e54cb-139">The process used by two key-exchange parties is as follows:</span></span>

-   <span data-ttu-id="e54cb-140">Beide Parteien stimmen den Diffie-Hellman Parametern zu, bei denen es sich um eine Primzahl (P) und eine Generator Nummer (G) handelt.</span><span class="sxs-lookup"><span data-stu-id="e54cb-140">Both parties agree to the Diffie-Hellman parameters which are a prime number (P) and a generator number (G).</span></span>
-   <span data-ttu-id="e54cb-141">Partei 1 sendet den Diffie-Hellman öffentlichen Schlüssel an Partei 2.</span><span class="sxs-lookup"><span data-stu-id="e54cb-141">Party 1 sends its Diffie-Hellman public key to party 2.</span></span>
-   <span data-ttu-id="e54cb-142">Partei 2 berechnet den geheimen Sitzungsschlüssel anhand der Informationen, die in seinem privaten Schlüssel und dem öffentlichen Schlüssel von Partei 1 enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e54cb-142">Party 2 computes the secret session key by using the information contained in its private key and party 1's public key.</span></span>
-   <span data-ttu-id="e54cb-143">Partei 2 sendet ihren Diffie-Hellman öffentlichen Schlüssel an Partei 1.</span><span class="sxs-lookup"><span data-stu-id="e54cb-143">Party 2 sends its Diffie-Hellman public key to party 1.</span></span>
-   <span data-ttu-id="e54cb-144">Partei 1 berechnet den geheimen Sitzungsschlüssel anhand der Informationen, die in seinem privaten Schlüssel und dem öffentlichen Schlüssel von Partei 2 enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e54cb-144">Party 1 computes the secret session key by using the information contained in its private key and party 2's public key.</span></span>
-   <span data-ttu-id="e54cb-145">Beide Parteien verfügen jetzt über denselben Sitzungsschlüssel, der zum Verschlüsseln und Entschlüsseln von Daten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e54cb-145">Both parties now have the same session key, which can be used for encrypting and decrypting data.</span></span> <span data-ttu-id="e54cb-146">Die hierfür erforderlichen Schritte werden im folgenden Verfahren beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e54cb-146">The steps necessary for this are shown in the following procedure.</span></span>

<span data-ttu-id="e54cb-147">**So bereiten Sie einen Diffie-Hellman öffentlichen Schlüssel für die Übertragung vor**</span><span class="sxs-lookup"><span data-stu-id="e54cb-147">**To prepare a Diffie-Hellman public key for transmission**</span></span>

1.  <span data-ttu-id="e54cb-148">Aufrufen der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion, um ein Handle für den Kryptografieanbieter von Microsoft Diffie-Hellman zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e54cb-148">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="e54cb-149">Erstellen Sie einen Diffie-Hellman Schlüssel, indem Sie die Funktion [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) aufrufen, um einen neuen Schlüssel zu erstellen, oder indem Sie die Funktion [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) aufrufen, um einen vorhandenen Schlüssel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e54cb-149">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="e54cb-150">Rufen Sie die erforderliche Größe für das Diffie-Hellman Schlüsselblob ab, indem Sie den [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)aufrufen und **null** für den *pbData* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="e54cb-150">Get the size needed to hold the Diffie-Hellman key BLOB by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), passing **NULL** for the *pbData* parameter.</span></span> <span data-ttu-id="e54cb-151">Die erforderliche Größe wird in " *pdwdatalen*" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e54cb-151">The required size will be returned in *pdwDataLen*.</span></span>
4.  <span data-ttu-id="e54cb-152">Arbeitsspeicher für das Schlüssel-BLOB zuweisen.</span><span class="sxs-lookup"><span data-stu-id="e54cb-152">Allocate memory for the key BLOB.</span></span>
5.  <span data-ttu-id="e54cb-153">Erstellen Sie ein [*BLOB für den öffentlichen Schlüssel*](../secgloss/p-gly.md) Diffie-Hellman, indem Sie die Funktion [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) aufrufen, indem Sie **PublicKeyBlob** im Parameter *dwblobtype* und das Handle an den Diffie-Hellman Schlüssel im *HKEY* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="e54cb-153">Create a Diffie-Hellman [*public key BLOB*](../secgloss/p-gly.md) by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, passing **PUBLICKEYBLOB** in the *dwBlobType* parameter and the handle to the Diffie-Hellman key in the *hKey* parameter.</span></span> <span data-ttu-id="e54cb-154">Dieser Funktions Aufrufvorgang bewirkt die Berechnung des Werts des öffentlichen Schlüssels (G ^ X) mod P.</span><span class="sxs-lookup"><span data-stu-id="e54cb-154">This function call causes the calculation of the public key value, (G^X) mod P.</span></span>
6.  <span data-ttu-id="e54cb-155">Wenn alle vorhergehenden Funktionsaufrufe erfolgreich waren, kann das BLOB des Diffie-Hellman öffentlichen Schlüssels jetzt codiert und übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="e54cb-155">If all the preceding function calls were successful, the Diffie-Hellman public key BLOB is now ready to be encoded and transmitted.</span></span>

<span data-ttu-id="e54cb-156">**So importieren Sie einen Diffie-Hellman öffentlichen Schlüssel und berechnen den geheimen Sitzungsschlüssel**</span><span class="sxs-lookup"><span data-stu-id="e54cb-156">**To import a Diffie-Hellman public key and calculate the secret session key**</span></span>

1.  <span data-ttu-id="e54cb-157">Aufrufen der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion, um ein Handle für den Kryptografieanbieter von Microsoft Diffie-Hellman zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e54cb-157">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="e54cb-158">Erstellen Sie einen Diffie-Hellman Schlüssel, indem Sie die Funktion [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) aufrufen, um einen neuen Schlüssel zu erstellen, oder indem Sie die Funktion [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) aufrufen, um einen vorhandenen Schlüssel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e54cb-158">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="e54cb-159">Um den Diffie-Hellman öffentlichen Schlüssel in den CSP zu importieren, müssen Sie die Funktion [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) aufrufen und einen Zeiger auf das BLOB des öffentlichen Schlüssels im *pbData* -Parameter, die Länge des BLOBs im Parameter *dwdatalen* und das Handle für den Diffie-Hellman Schlüssel im *hpubkey* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="e54cb-159">To import the Diffie-Hellman public key into the CSP, call the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function, passing a pointer to the public key BLOB in the *pbData* parameter, the length of the BLOB in the *dwDataLen* parameter, and the handle to the Diffie-Hellman key in the *hPubKey* parameter.</span></span> <span data-ttu-id="e54cb-160">Dies bewirkt, dass die Berechnung (Y ^ X) mod P ausgeführt wird. auf diese Weise wird der gemeinsame geheime Schlüssel erstellt und der [*Schlüsselaustausch*](../secgloss/e-gly.md)abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e54cb-160">This causes the calculation, (Y^X) mod P, to be performed, thus creating the shared, secret key and completing the [*key exchange*](../secgloss/e-gly.md).</span></span> <span data-ttu-id="e54cb-161">Dieser Funktions aufruter gibt ein Handle für den neuen geheimen Schlüssel, den Sitzungsschlüssel im *HKEY* -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="e54cb-161">This function call returns a handle to the new, secret, session key in the *hKey* parameter.</span></span>
4.  <span data-ttu-id="e54cb-162">An diesem Punkt ist der importierte Diffie-Hellman vom Typ **calg \_ agreedkey \_ any**.</span><span class="sxs-lookup"><span data-stu-id="e54cb-162">At this point, the imported Diffie-Hellman is of type **CALG\_AGREEDKEY\_ANY**.</span></span> <span data-ttu-id="e54cb-163">Bevor der Schlüssel verwendet werden kann, muss er in einen Sitzungs Schlüsseltyp konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="e54cb-163">Before the key can be used, it must be converted into a session key type.</span></span> <span data-ttu-id="e54cb-164">Dies wird erreicht, indem die [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) -Funktion mit *dwparam* auf **KP \_ algid** festgelegt und *pbData* auf einen Zeiger auf einen [**ALG- \_ ID**](alg-id.md) -Wert festgelegt wird, der einen Sitzungsschlüssel darstellt, z. b. **calg \_ RC4**.</span><span class="sxs-lookup"><span data-stu-id="e54cb-164">This is accomplished by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function with *dwParam* set to **KP\_ALGID** and with *pbData* set to a pointer to a [**ALG\_ID**](alg-id.md) value that represents a session key, such as **CALG\_RC4**.</span></span> <span data-ttu-id="e54cb-165">Der Schlüssel muss konvertiert werden, bevor der gemeinsam verwendete Schlüssel in der [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) -Funktion oder der [**cryptentschlpt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e54cb-165">The key must be converted before using the shared key in the [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) or [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) function.</span></span> <span data-ttu-id="e54cb-166">Aufrufe an eine dieser Funktionen, bevor der Schlüsseltyp umgewandelt wird, können nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e54cb-166">Calls made to either of these functions prior to converting the key type will fail.</span></span>
5.  <span data-ttu-id="e54cb-167">Der geheime Sitzungsschlüssel kann jetzt für die Verschlüsselung oder Entschlüsselung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e54cb-167">The secret session key is now ready to be used for encryption or decryption.</span></span>
6.  <span data-ttu-id="e54cb-168">Wenn der Schlüssel nicht mehr benötigt wird, zerstören Sie den Schlüssel Handle durch Aufrufen der [**cryptdestroykey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e54cb-168">When the key is no longer needed, destroy the key handle by calling the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function.</span></span>

## <a name="exporting-a-diffie-hellman-private-key"></a><span data-ttu-id="e54cb-169">Exportieren eines Diffie-Hellman privaten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="e54cb-169">Exporting a Diffie-Hellman Private Key</span></span>

<span data-ttu-id="e54cb-170">Um einen Diffie-Hellman privaten Schlüssel zu exportieren, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="e54cb-170">To export a Diffie-Hellman private key, perform the following steps:</span></span>

1.  <span data-ttu-id="e54cb-171">Aufrufen der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion, um ein Handle für den Kryptografieanbieter von Microsoft Diffie-Hellman zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e54cb-171">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="e54cb-172">Erstellen Sie einen Diffie-Hellman Schlüssel, indem Sie die Funktion [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) aufrufen, um einen neuen Schlüssel zu erstellen, oder indem Sie die Funktion [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) aufrufen, um einen vorhandenen Schlüssel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e54cb-172">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="e54cb-173">Erstellen Sie einen Diffie-Hellman [*privaten Schlüsselblob*](../secgloss/p-gly.md) , indem Sie die [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) -Funktion aufrufen und dabei **privatekeyblob** im Parameter *dwblobtype* und das Handle an den Diffie-Hellman Schlüssel im *HKEY* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="e54cb-173">Create a Diffie-Hellman [*private key BLOB*](../secgloss/p-gly.md) by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, passing **PRIVATEKEYBLOB** in the *dwBlobType* parameter and the handle to the Diffie-Hellman key in the *hKey* parameter.</span></span>
4.  <span data-ttu-id="e54cb-174">Wenn das Schlüssel Handle nicht mehr benötigt wird, können Sie die Funktion " [**cryptdestroykey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) " aufrufen, um das Schlüssel Handle zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="e54cb-174">When the key handle is no longer needed, call the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function to destroy the key handle.</span></span>

## <a name="example-code"></a><span data-ttu-id="e54cb-175">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="e54cb-175">Example Code</span></span>

<span data-ttu-id="e54cb-176">Im folgenden Beispiel wird gezeigt, wie ein Diffie-Hellman Schlüssel erstellt, exportiert, importiert und verwendet wird, um einen Schlüsselaustausch auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e54cb-176">The following example shows how to create, export, import, and use a Diffie-Hellman key to perform a key exchange.</span></span>


```C++
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// The key size, in bits.
#define DHKEYSIZE 512

// Prime in little-endian format.
static const BYTE g_rgbPrime[] = 
{
    0x91, 0x02, 0xc8, 0x31, 0xee, 0x36, 0x07, 0xec, 
    0xc2, 0x24, 0x37, 0xf8, 0xfb, 0x3d, 0x69, 0x49, 
    0xac, 0x7a, 0xab, 0x32, 0xac, 0xad, 0xe9, 0xc2, 
    0xaf, 0x0e, 0x21, 0xb7, 0xc5, 0x2f, 0x76, 0xd0, 
    0xe5, 0x82, 0x78, 0x0d, 0x4f, 0x32, 0xb8, 0xcb,
    0xf7, 0x0c, 0x8d, 0xfb, 0x3a, 0xd8, 0xc0, 0xea, 
    0xcb, 0x69, 0x68, 0xb0, 0x9b, 0x75, 0x25, 0x3d,
    0xaa, 0x76, 0x22, 0x49, 0x94, 0xa4, 0xf2, 0x8d 
};

// Generator in little-endian format.
static BYTE g_rgbGenerator[] = 
{
    0x02, 0x88, 0xd7, 0xe6, 0x53, 0xaf, 0x72, 0xc5,
    0x8c, 0x08, 0x4b, 0x46, 0x6f, 0x9f, 0x2e, 0xc4,
    0x9c, 0x5c, 0x92, 0x21, 0x95, 0xb7, 0xe5, 0x58, 
    0xbf, 0xba, 0x24, 0xfa, 0xe5, 0x9d, 0xcb, 0x71, 
    0x2e, 0x2c, 0xce, 0x99, 0xf3, 0x10, 0xff, 0x3b,
    0xcb, 0xef, 0x6c, 0x95, 0x22, 0x55, 0x9d, 0x29,
    0x00, 0xb5, 0x4c, 0x5b, 0xa5, 0x63, 0x31, 0x41,
    0x13, 0x0a, 0xea, 0x39, 0x78, 0x02, 0x6d, 0x62
};

BYTE g_rgbData[] = {0x01, 0x02, 0x03, 0x04,    0x05, 0x06, 0x07, 0x08};

int _tmain(int argc, _TCHAR* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    BOOL fReturn;
    HCRYPTPROV hProvParty1 = NULL; 
    HCRYPTPROV hProvParty2 = NULL; 
    DATA_BLOB P;
    DATA_BLOB G;
    HCRYPTKEY hPrivateKey1 = NULL;
    HCRYPTKEY hPrivateKey2 = NULL;
    PBYTE pbKeyBlob1 = NULL;
    PBYTE pbKeyBlob2 = NULL;
    HCRYPTKEY hSessionKey1 = NULL;
    HCRYPTKEY hSessionKey2 = NULL;
    PBYTE pbData = NULL;

    /************************
    Construct data BLOBs for the prime and generator. The P and G 
    values, represented by the g_rgbPrime and g_rgbGenerator arrays 
    respectively, are shared values that have been agreed to by both 
    parties.
    ************************/
    P.cbData = DHKEYSIZE/8;
    P.pbData = (BYTE*)(g_rgbPrime);

    G.cbData = DHKEYSIZE/8;
    G.pbData = (BYTE*)(g_rgbGenerator);

    /************************
    Create the private Diffie-Hellman key for party 1. 
    ************************/
    // Acquire a provider handle for party 1.
    fReturn = CryptAcquireContext(
        &hProvParty1, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 1.
    fReturn = CryptGenKey(
        hProvParty1, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Create the private Diffie-Hellman key for party 2. 
    ************************/
    // Acquire a provider handle for party 2.
    fReturn = CryptAcquireContext(
        &hProvParty2, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 2.
    fReturn = CryptGenKey(
        hProvParty2, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 1's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen1;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob1 = (PBYTE)malloc(dwDataLen1)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob1,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 2's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen2;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob2 = (PBYTE)malloc(dwDataLen2)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob2,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Party 1 imports party 2's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty1,
        pbKeyBlob2,
        dwDataLen2,
        hPrivateKey1,
        0,
        &hSessionKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }
    
    /************************
    Party 2 imports party 1's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty2,
        pbKeyBlob1,
        dwDataLen1,
        hPrivateKey2,
        0,
        &hSessionKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Convert the agreed keys to symmetric keys. They are currently of 
    the form CALG_AGREEDKEY_ANY. Convert them to CALG_RC4.
    ************************/
    ALG_ID Algid = CALG_RC4;

    // Enable the party 1 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey1,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Enable the party 2 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey2,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Encrypt some data with party 1's session key. 
    ************************/
    // Get the size.
    DWORD dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        NULL, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate a buffer to hold the encrypted data.
    pbData = (PBYTE)malloc(dwLength);
    if(!pbData)
    {
        goto ErrorExit;
    }

    // Copy the unencrypted data to the buffer. The data will be 
    // encrypted in place.
    memcpy(pbData, g_rgbData, sizeof(g_rgbData)); 

    // Encrypt the data.
    dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        pbData, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }
  
    /************************
    Decrypt the data with party 2's session key. 
    ************************/
    dwLength = sizeof(g_rgbData);
    fReturn = CryptDecrypt(
        hSessionKey2,
        0,
        TRUE,
        0,
        pbData,
        &dwLength);
    if(!fReturn)
    {
        goto ErrorExit;
    }


ErrorExit:
    if(pbData)
    {
        free(pbData);
        pbData = NULL;
    }

    if(hSessionKey2)
    {
        CryptDestroyKey(hSessionKey2);
        hSessionKey2 = NULL;
    }

    if(hSessionKey1)
    {
        CryptDestroyKey(hSessionKey1);
        hSessionKey1 = NULL;
    }

    if(pbKeyBlob2)
    {
        free(pbKeyBlob2);
        pbKeyBlob2 = NULL;
    }

    if(pbKeyBlob1)
    {
        free(pbKeyBlob1);
        pbKeyBlob1 = NULL;
    }

    if(hPrivateKey2)
    {
        CryptDestroyKey(hPrivateKey2);
        hPrivateKey2 = NULL;
    }

    if(hPrivateKey1)
    {
        CryptDestroyKey(hPrivateKey1);
        hPrivateKey1 = NULL;
    }

    if(hProvParty2)
    {
        CryptReleaseContext(hProvParty2, 0);
        hProvParty2 = NULL;
    }

    if(hProvParty1)
    {
        CryptReleaseContext(hProvParty1, 0);
        hProvParty1 = NULL;
    }

    return 0;
}
```



 

 
