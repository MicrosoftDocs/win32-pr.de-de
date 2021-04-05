---
title: Win32-Fehler Codes für ADSI
description: Standard-Win32-Fehlercodes werden auch zum Zurückgeben von ADSI-Fehlermeldungen verwendet.
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- Win32-Fehler Codes für ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47151a3a1619a7f224dc0b9b7f0871813a346a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707349"
---
# <a name="win32-error-codes-for-adsi"></a><span data-ttu-id="b32b4-104">Win32-Fehler Codes für ADSI</span><span class="sxs-lookup"><span data-stu-id="b32b4-104">Win32 Error Codes for ADSI</span></span>

<span data-ttu-id="b32b4-105">Standard-Win32-Fehlercodes werden auch zum Zurückgeben von ADSI-Fehlermeldungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b32b4-105">Standard Win32 error codes are also used to return ADSI error messages.</span></span> <span data-ttu-id="b32b4-106">Insbesondere ordnet der ADSI LDAP-Anbieter alle LDAP-Fehlercodes den Win32-Fehlercodes zu.</span><span class="sxs-lookup"><span data-stu-id="b32b4-106">Specifically, the ADSI LDAP provider maps all the LDAP error codes to Win32 error codes.</span></span> <span data-ttu-id="b32b4-107">Die **HRESULT** -Werte dieser Fehlercodes haben das Format 0x8007xxxx, wobei die letzten vier hexadezimalen Ziffern xxxx den **DWORD** -Werten des entsprechenden Win32-Fehlercodes entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b32b4-107">The **HRESULT** values of these error codes are of the 0x8007XXXX format, where the last four hexadecimal digits, XXXX, corresponds to the **DWORD** values of the appropriate Win32 error code.</span></span> <span data-ttu-id="b32b4-108">Der ADSI-Fehlerwert 0x80072020 gibt z. b. den Win32-Fehlerwert 0x2020 in Hexadezimal oder 8224 als Dezimalwert an.</span><span class="sxs-lookup"><span data-stu-id="b32b4-108">For example, the ADSI error value 0x80072020 gives the Win32 error value of 0x2020 in hexadecimal or 8224 in decimal.</span></span>

<span data-ttu-id="b32b4-109">Um den **HRESULT** -Wert eines von der Anwendung zurückgegebenen ADSI-Fehlercodes in den entsprechenden Win32- **DWORD** -Wert zu konvertieren, wie in den Header Dateien oben definiert, verwenden Sie das folgende Verfahren.</span><span class="sxs-lookup"><span data-stu-id="b32b4-109">To convert the **HRESULT** value of an ADSI error code, returned by your application, to the corresponding the Win32 error **DWORD** value, as defined in the header files above, use the following procedure.</span></span>

<span data-ttu-id="b32b4-110">Die meisten Win32-Fehlercodes für ADSI sind in WinError. h oder lmerr. h definiert.</span><span class="sxs-lookup"><span data-stu-id="b32b4-110">Most of the Win32 error codes for ADSI are defined in Winerror.h or Lmerr.h.</span></span> <span data-ttu-id="b32b4-111">Die Fehler Werte werden in diesen Dateien als Dezimalwerte aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b32b4-111">The error values are listed as decimal values in these files.</span></span>

<span data-ttu-id="b32b4-112">**So konvertieren Sie den **HRESULT** -Wert eines ADSI-Fehlercodes in den entsprechenden Win32-Fehler **DWORD** -Wert**</span><span class="sxs-lookup"><span data-stu-id="b32b4-112">**To convert the **HRESULT** value of an ADSI error code to the corresponding the Win32 error **DWORD** value**</span></span>

1.  <span data-ttu-id="b32b4-113">Konvertieren Sie den **HRESULT** -Wert in eine hexadezimale Zahl, wenn Sie mit einem Dezimalwert beginnen, wie Sie möglicherweise von einer Visual Basic Anwendung erhalten.</span><span class="sxs-lookup"><span data-stu-id="b32b4-113">Convert the **HRESULT** value to a hexadecimal number if starting with a decimal value as you may get from a Visual Basic application.</span></span>
2.  <span data-ttu-id="b32b4-114">Drop The 0x8007 Part erzeugt den Rest.</span><span class="sxs-lookup"><span data-stu-id="b32b4-114">Drop the 0x8007 part produce the remainder.</span></span>
3.  <span data-ttu-id="b32b4-115">Konvertiert den Rest in eine Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="b32b4-115">Convert the remainder to a decimal number.</span></span>
4.  <span data-ttu-id="b32b4-116">Suchen Sie in WinError. h nach dem Dezimaltrennzeichen.</span><span class="sxs-lookup"><span data-stu-id="b32b4-116">Look up the decimal remainder in Winerror.h.</span></span>
5.  <span data-ttu-id="b32b4-117">Wenn Sie in WinError. h nicht gefunden werden, subtrahieren Sie 2100 vom Dezimaltrennzeichen, und suchen Sie das Ergebnis in lmerr. h.</span><span class="sxs-lookup"><span data-stu-id="b32b4-117">If not found in Winerror.h, subtract 2100 from the decimal remainder and look up the result in Lmerr.h.</span></span>

<span data-ttu-id="b32b4-118">ADSI 2,0 ordnet die LDAP-Fehlercodes einer Reihe von Win32-Fehlercodes zu, die sich von der in ADSI für Windows 2000 und dem DS-Client verwendeten Win32-Fehlercodes unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="b32b4-118">ADSI 2.0 maps the LDAP error codes to a set of Win32 error codes that is different from that used in ADSI for Windows 2000 and DS Client.</span></span> <span data-ttu-id="b32b4-119">Die Unterschiede sind in aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="b32b4-119">The differences are listed in:</span></span>

-   [<span data-ttu-id="b32b4-120">Win32-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="b32b4-120">Win32 Error Codes</span></span>](win32-error-codes.md)
-   [<span data-ttu-id="b32b4-121">Win32-Fehler Codes für ADSI 2,0</span><span class="sxs-lookup"><span data-stu-id="b32b4-121">Win32 Error Codes for ADSI 2.0</span></span>](win32-error-codes-for-adsi-2-0.md)

 

 




