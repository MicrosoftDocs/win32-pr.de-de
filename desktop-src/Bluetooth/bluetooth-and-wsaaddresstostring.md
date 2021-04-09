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
# <a name="bluetooth-and-wsaaddresstostring"></a>Bluetooth und wsaadresssstostring

Die Windows Sockets-Funktion von [**wsaadresssstostring**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) wird verwendet, um eine Bluetooth-Geräteadresse in eine Zeichenfolge zu konvertieren, die wiederum über die [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur beim Abrufen von Geräte Dienst Informationen für die [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion bereitgestellt wird.

Obwohl eine Bluetooth-Geräteadresse in einen 20-Zeichen-Puffer passt, gibt die [**wsaaddresssstostring**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) -Funktion derzeit **wsaefault** für Bluetooth-Geräte Adressen zurück, es sei denn, der Puffer und der angegebene *lpdwaddressstringlength* -Wert sind auf eine Zeichen Länge von 40 festgelegt.

> [!Note]  
> Wenn **wsaefault** von [**wsaadresssstostring**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) als Ergebnis eines nicht ausreichenden Puffers zurückgegeben wird, wird der *lpdwaddressstringlength* -Parameter nicht mit der für den Vorgang erforderlichen Puffergröße aktualisiert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Wsaadresssstostring**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[Bluetooth und wsalookupservicebegin](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[Bluetooth und wsaqueryset](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 