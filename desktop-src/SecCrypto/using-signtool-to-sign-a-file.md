---
description: Erläutert, wie SignTool verwendet wird, um eine Datei zu signieren.
ms.assetid: fa8ee4d3-8927-4f7d-a09e-dbcf75a164d3
title: Signieren einer Datei mithilfe von SignTool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089026cde629278e5c6ac033164c2a9d26528917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130236"
---
# <a name="using-signtool-to-sign-a-file"></a><span data-ttu-id="fb2ce-103">Signieren einer Datei mithilfe von SignTool</span><span class="sxs-lookup"><span data-stu-id="fb2ce-103">Using SignTool to Sign a File</span></span>

<span data-ttu-id="fb2ce-104">Mit dem folgenden Befehl wird die Datei mit dem Namen MyControl.exe unter Verwendung eines [*Zertifikats*](../secgloss/c-gly.md) signiert, das in einer PFX-Datei (Personal Information Exchange) gespeichert ist:</span><span class="sxs-lookup"><span data-stu-id="fb2ce-104">The following command signs the file named MyControl.exe using a [*certificate*](../secgloss/c-gly.md) stored in a Personal Information Exchange (PFX) file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

<span data-ttu-id="fb2ce-105">Mit dem folgenden Befehl wird die Datei mithilfe eines Zertifikats signiert, das in einer Kenn Wort geschützten PFX-Datei gespeichert ist:</span><span class="sxs-lookup"><span data-stu-id="fb2ce-105">The following command signs the file using a certificate stored in a password-protected PFX file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> <span data-ttu-id="fb2ce-106">Stellen Sie sicher, dass Sie das Kennwort richtig schützen.</span><span class="sxs-lookup"><span data-stu-id="fb2ce-106">Ensure that you properly protect the password.</span></span>

 

<span data-ttu-id="fb2ce-107">Der folgende Befehl signiert und Zeitstempel für die Datei:</span><span class="sxs-lookup"><span data-stu-id="fb2ce-107">The following command signs and time stamps the file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> <span data-ttu-id="fb2ce-108">Informationen zum Zeitstempel einer Datei, nachdem Sie bereits signiert wurde, finden Sie unter [Hinzufügen von Zeitstempeln zu zuvor signierten Dateien](adding-time-stamps-to-previously-signed-files.md).</span><span class="sxs-lookup"><span data-stu-id="fb2ce-108">For information about time stamping a file after it has already been signed, see [Adding Time Stamps to Previously Signed Files](adding-time-stamps-to-previously-signed-files.md).</span></span>

 

<span data-ttu-id="fb2ce-109">Mit dem folgenden Befehl wird die Datei mithilfe eines Zertifikats in "My Store" mit dem Antragsteller Namen "My Company Publisher" signiert:</span><span class="sxs-lookup"><span data-stu-id="fb2ce-109">The following command signs the file using a certificate located in the My store with a subject name of My Company Publisher:</span></span>

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

<span data-ttu-id="fb2ce-110">Der folgende Befehl signiert ein ActiveX-Steuerelement und stellt Informationen bereit, die von Internet Explorer angezeigt werden, wenn der Benutzer aufgefordert wird, das-Steuerelement zu installieren:</span><span class="sxs-lookup"><span data-stu-id="fb2ce-110">The following command signs an ActiveX control and provides information that is displayed by Internet Explorer when the user is prompted to install the control:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

<span data-ttu-id="fb2ce-111">Mit dem folgenden Befehl wird die Datei mithilfe eines Zertifikats signiert, dessen Informationen zum [*privaten Schlüssel*](../secgloss/p-gly.md) von einem Hardware kryptografiemodul geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="fb2ce-111">The following command signs the file using a certificate whose [*private key*](../secgloss/p-gly.md) information is protected by a hardware cryptography module.</span></span> <span data-ttu-id="fb2ce-112">Nehmen Sie beispielsweise an, dass das Zertifikat mit dem Namen "My High-Value Certificate" einen privaten Schlüssel enthält, der in einem Hardware kryptografiemodul installiert ist, und dass das Zertifikat ordnungsgemäß installiert ist.</span><span class="sxs-lookup"><span data-stu-id="fb2ce-112">For example purposes, assume that the certificate called "My High-Value Certificate," has a private key installed in a hardware cryptography module, and the certificate is properly installed.</span></span>

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

<span data-ttu-id="fb2ce-113">Mit dem folgenden Befehl wird die Datei mithilfe eines Zertifikats signiert, dessen Informationen zum [*privaten Schlüssel*](../secgloss/p-gly.md) von einem Hardware kryptografiemodul geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="fb2ce-113">The following command signs the file using a certificate whose [*private key*](../secgloss/p-gly.md) information is protected by a hardware cryptography module.</span></span> <span data-ttu-id="fb2ce-114">Für den [*Zertifizierungs*](../secgloss/c-gly.md) stellen Speicher (ca) ist ein Computerspeicher angegeben.</span><span class="sxs-lookup"><span data-stu-id="fb2ce-114">A computer store is specified for the [*certification authority*](../secgloss/c-gly.md) (CA) store.</span></span>

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

<span data-ttu-id="fb2ce-115">Mit dem folgenden Befehl wird die Datei mithilfe eines Zertifikats signiert, das in einer Datei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="fb2ce-115">The following command signs the file using a certificate stored in a file.</span></span> <span data-ttu-id="fb2ce-116">Die Informationen zum privaten Schlüssel werden durch ein Hardware kryptografiemodul geschützt, und der [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) und der [*Schlüssel Container*](../secgloss/k-gly.md) werden anhand des Namens angegeben.</span><span class="sxs-lookup"><span data-stu-id="fb2ce-116">The private key information is protected by a hardware cryptography module, and the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP)and [*key container*](../secgloss/k-gly.md) are specified by name.</span></span> <span data-ttu-id="fb2ce-117">Dieser Befehl ist nützlich, wenn das Zertifikat nicht ordnungsgemäß installiert ist.</span><span class="sxs-lookup"><span data-stu-id="fb2ce-117">This command is useful if the certificate is not properly installed.</span></span>

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

<span data-ttu-id="fb2ce-118">[SignTool](signtool.md) gibt Befehlszeilen Text zurück, der das Ergebnis des Signatur Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="fb2ce-118">[SignTool](signtool.md) returns command line text that states the result of the signing operation.</span></span> <span data-ttu-id="fb2ce-119">Außerdem gibt SignTool den Exitcode 0 (null) für die erfolgreiche Ausführung zurück, einen für die fehlgeschlagene Ausführung und zwei für die Ausführung, die mit Warnungen abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="fb2ce-119">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="fb2ce-120">Weitere Informationen zum Überprüfen der Signatur einer Datei finden [Sie unter Verwenden von SignTool zum Überprüfen einer Datei Signatur](using-signtool-to-verify-a-file-signature.md).</span><span class="sxs-lookup"><span data-stu-id="fb2ce-120">For information about verifying a file's signature, see [Using SignTool to Verify a File Signature](using-signtool-to-verify-a-file-signature.md).</span></span> <span data-ttu-id="fb2ce-121">Weitere Informationen zum Hinzufügen eines Zeitstempels, wenn die Datei bereits signiert wurde, finden [Sie unter Hinzufügen von Zeitstempeln zu zuvor signierten Dateien](adding-time-stamps-to-previously-signed-files.md).</span><span class="sxs-lookup"><span data-stu-id="fb2ce-121">For information about adding a time stamp if the file has already been signed, see [Adding Time Stamps to Previously Signed Files](adding-time-stamps-to-previously-signed-files.md).</span></span> <span data-ttu-id="fb2ce-122">Weitere Informationen zu [SignTool](signtool.md)finden Sie unter [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="fb2ce-122">For additional information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 
