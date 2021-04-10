---
title: LDAP-Fehler Codes für ADSI
description: Wenn ein LDAP-Server einen Fehler generiert und den Fehler an den Client übergibt, wird der Fehler dann vom LDAP-Client in eine Zeichenfolge übersetzt.
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149abf4562b0e35067149fb69c9a1ec1304cc528
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855284"
---
# <a name="ldap-error-codes-for-adsi"></a><span data-ttu-id="dc80a-103">LDAP-Fehler Codes für ADSI</span><span class="sxs-lookup"><span data-stu-id="dc80a-103">LDAP Error Codes for ADSI</span></span>

<span data-ttu-id="dc80a-104">Wenn ein LDAP-Server einen Fehler generiert und den Fehler an den Client übergibt, wird der Fehler dann vom LDAP-Client in eine Zeichenfolge übersetzt.</span><span class="sxs-lookup"><span data-stu-id="dc80a-104">When an LDAP server generates an error and passes the error to the client, the error is then translated into a string by the LDAP client.</span></span>

<span data-ttu-id="dc80a-105">Diese Methode ähnelt den [Win32-Fehlercodes für ADSI](win32-error-codes-for-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="dc80a-105">This method is similar to [Win32 error codes for ADSI](win32-error-codes-for-adsi.md).</span></span> <span data-ttu-id="dc80a-106">In diesem Beispiel ist der Client Fehlercode der Win32-Fehler 0x80072020.</span><span class="sxs-lookup"><span data-stu-id="dc80a-106">In this example, the client error code is the WIN32 error 0x80072020.</span></span>

<span data-ttu-id="dc80a-107">**So bestimmen Sie die LDAP-Fehlercodes für ADSI**</span><span class="sxs-lookup"><span data-stu-id="dc80a-107">**To Determine the LDAP error codes for ADSI**</span></span>

1.  <span data-ttu-id="dc80a-108">Legen Sie den 8007 aus dem Win32-Fehlercode ab.</span><span class="sxs-lookup"><span data-stu-id="dc80a-108">Drop the 8007 from the WIN32 error code.</span></span> <span data-ttu-id="dc80a-109">Im Beispiel ist der verbleibende Hexadezimalwert 2020.</span><span class="sxs-lookup"><span data-stu-id="dc80a-109">In the example, the remaining hex value is 2020.</span></span>
2.  <span data-ttu-id="dc80a-110">Konvertiert den verbleibenden Hexadezimalwert in einen Dezimalwert.</span><span class="sxs-lookup"><span data-stu-id="dc80a-110">Convert the remaining hex value to a decimal value.</span></span> <span data-ttu-id="dc80a-111">Im Beispiel wird der verbleibende Hexadezimalwert 2020 in den Dezimalwert 8224 konvertiert.</span><span class="sxs-lookup"><span data-stu-id="dc80a-111">In the example, the remaining hex value 2020 converts to the decimal value 8224.</span></span>
3.  <span data-ttu-id="dc80a-112">Suchen Sie in der Datei "Winerror. h" nach der Definition des Dezimal Werts.</span><span class="sxs-lookup"><span data-stu-id="dc80a-112">Search in the WinError.h file for the definition of the decimal value.</span></span> <span data-ttu-id="dc80a-113">Im Beispiel entspricht 8224l dem Fehler Fehler DS- **\_ \_ Vorgangs \_ Fehler**.</span><span class="sxs-lookup"><span data-stu-id="dc80a-113">In the example, 8224L corresponds to the error **ERROR\_DS\_OPERATIONS\_ERROR**.</span></span>
4.  <span data-ttu-id="dc80a-114">Ersetzen Sie den Präfix **Fehler \_ DS** durch **LDAP \_**.</span><span class="sxs-lookup"><span data-stu-id="dc80a-114">Replace the prefix **ERROR\_DS** with **LDAP\_**.</span></span> <span data-ttu-id="dc80a-115">Im Beispiel ist die neue Definition LDAP- **\_ Vorgangs \_ Fehler**.</span><span class="sxs-lookup"><span data-stu-id="dc80a-115">In the example, the new definition is **LDAP\_OPERATIONS\_ERROR**.</span></span>
5.  <span data-ttu-id="dc80a-116">Suchen Sie in der Datei winldap. h nach dem Wert der LDAP-Fehler Definition.</span><span class="sxs-lookup"><span data-stu-id="dc80a-116">Search in the Winldap.h file for the value of the LDAP error definition.</span></span> <span data-ttu-id="dc80a-117">Im Beispiel lautet der Wert von **LDAP- \_ Vorgangs \_ Fehler** in der Datei "winldap. h" 0x01.</span><span class="sxs-lookup"><span data-stu-id="dc80a-117">In the example, the value of **LDAP\_OPERATIONS\_ERROR** in the Winldap.h file is 0x01.</span></span>

 

 




