---
title: Bluetooth und wsaadresssstostring
description: Die Windows Sockets-Funktion von wsaadresssstostring wird verwendet, um eine Bluetooth-Geräteadresse in eine Zeichenfolge zu konvertieren, die wiederum über die wsaqueryset-Struktur beim Abrufen von Geräte Dienst Informationen für die wsalookupservicebegin-Funktion bereitgestellt wird.
ms.assetid: 3489d29a-2b64-4051-b579-57878efc0c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e8a9ae3ea6a0f853619a3f3610a64204ad3c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039070"
---
# <a name="bluetooth-and-wsaaddresstostring"></a><span data-ttu-id="bc168-103">Bluetooth und wsaadresssstostring</span><span class="sxs-lookup"><span data-stu-id="bc168-103">Bluetooth and WSAAddressToString</span></span>

<span data-ttu-id="bc168-104">Die Windows Sockets-Funktion von [**wsaadresssstostring**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) wird verwendet, um eine Bluetooth-Geräteadresse in eine Zeichenfolge zu konvertieren, die wiederum über die [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur beim Abrufen von Geräte Dienst Informationen für die [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bc168-104">The [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows Sockets function is used to convert a Bluetooth Device Address to a string, which is in turn provided to the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function via the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure when retrieving device service information.</span></span>

<span data-ttu-id="bc168-105">Obwohl eine Bluetooth-Geräteadresse in einen 20-Zeichen-Puffer passt, gibt die [**wsaaddresssstostring**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) -Funktion derzeit **wsaefault** für Bluetooth-Geräte Adressen zurück, es sei denn, der Puffer und der angegebene *lpdwaddressstringlength* -Wert sind auf eine Zeichen Länge von 40 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bc168-105">While a Bluetooth Device Address fits within a 20 character buffer, the [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) function currently returns **WSAEFAULT** for Bluetooth Device Addresses unless the buffer and the specified *lpdwAddressStringLength* value are set to a character length of 40.</span></span>

> [!Note]  
> <span data-ttu-id="bc168-106">Wenn **wsaefault** von [**wsaadresssstostring**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) als Ergebnis eines nicht ausreichenden Puffers zurückgegeben wird, wird der *lpdwaddressstringlength* -Parameter nicht mit der für den Vorgang erforderlichen Puffergröße aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bc168-106">When **WSAEFAULT** is returned by [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) as the result of an insufficient buffer, the *lpdwAddressStringLength* parameter is not updated with the buffer size required for the operation.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bc168-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bc168-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc168-108">**Wsaadresssstostring**</span><span class="sxs-lookup"><span data-stu-id="bc168-108">**WSAAddressToString**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[<span data-ttu-id="bc168-109">Bluetooth und wsalookupservicebegin</span><span class="sxs-lookup"><span data-stu-id="bc168-109">Bluetooth and WSALookupServiceBegin</span></span>](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="bc168-110">Bluetooth und wsaqueryset</span><span class="sxs-lookup"><span data-stu-id="bc168-110">Bluetooth and WSAQUERYSET</span></span>](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 