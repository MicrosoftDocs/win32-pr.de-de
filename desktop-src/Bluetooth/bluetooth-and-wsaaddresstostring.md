---
title: Bluetooth und WSAAddressToString
description: Die WSAAddressToString Windows Sockets-Funktion wird verwendet, um eine Bluetooth-Geräteadresse in eine Zeichenfolge zu konvertieren, die wiederum für die WSALookupServiceBegin-Funktion über die WSAQUERYSET-Struktur beim Abrufen von Gerätedienstinformationen bereitgestellt wird.
ms.assetid: 3489d29a-2b64-4051-b579-57878efc0c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bb49563355b3a85ff64d7168f77e8526ca1679cffaa565e7b9cd7070cf87f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004280"
---
# <a name="bluetooth-and-wsaaddresstostring"></a>Bluetooth und WSAAddressToString

Die [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows Sockets-Funktion wird verwendet, um eine Bluetooth-Geräteadresse in eine Zeichenfolge zu konvertieren, die wiederum für die [**WSALookupServiceBegin-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) über die [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) beim Abrufen von Gerätedienstinformationen bereitgestellt wird.

Während eine Bluetooth-Geräteadresse in einen Puffer mit 20 Zeichen passt, gibt die [**WSAAddressToString-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) derzeit **WSAEFAULT** für Bluetooth-Geräteadressen zurück, es sei denn, der Puffer und der angegebene *lpdwAddressStringLength-Wert* sind auf eine Zeichenlänge von 40 festgelegt.

> [!Note]  
> Wenn **WSAEFAULT** von [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) als Ergebnis eines unzureichenden Puffers zurückgegeben wird, wird der *lpdwAddressStringLength-Parameter* nicht mit der für den Vorgang erforderlichen Puffergröße aktualisiert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[Bluetooth und WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[Bluetooth und WSAQUERYSET](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 