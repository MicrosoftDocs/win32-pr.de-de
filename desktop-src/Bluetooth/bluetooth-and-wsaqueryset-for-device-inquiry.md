---
title: Bluetooth und wsaqueryset für Geräte Anfrage
description: Wird verwendet, um die Ermittlung von Geräten und Diensten im Bluetooth-Namespace (NS BTH) zu vereinfachen \_ .
ms.assetid: 0c0d26f7-b6c3-42a9-8c01-118278c381cc
keywords:
- Bluetooth und wsaqueryset für Geräte Anfrage Bluetooth
- Wsaqueryset Bluetooth für Geräte Anfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de7adf8c15907fe539ddac5133df08d68ee7c4f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727641"
---
# <a name="bluetooth-and-wsaqueryset-for-device-inquiry"></a>Bluetooth und wsaqueryset für Geräte Anfrage

In Bluetooth wird die [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur verwendet, um die Ermittlung von Geräten und Diensten im Bluetooth-Namespace (NS BTH) zu vereinfachen \_ .

Die [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion und die [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Funktion verwenden die [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur, um Informationen über den Geräte Abfrageprozess zu erhalten. In der folgenden Tabelle sind die Element Werte in der **wsaqueryset** -Struktur aufgelistet und beschrieben.

| Member                      | Eingabe für wsalookupservicebegin mit angegebenen Lup- \_ Containern                                                                                                                                              | Rückgabewert von WSALookupServiceNext                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**                  | Muss auf **sizeof**([**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)) festgelegt werden.                                                                                                                                       | **sizeof**([**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)) vom System zurückgegeben.                                                                                                                                                                                                                                                                                                                                                        |
| **dwoutputflags**           | Nicht verwendet.                                                                                                                                                                                                  | Möglicherweise ist mindestens eines der folgenden Flags festgelegt: **bthns- \_ Ergebnis \_ Geräte \_ Verbindung** gibt an, dass das Gerät verbunden ist.<br/> **Bthns \_ Ergebnis \_ Gerät \_ gespeichert** gibt an, dass das Gerät ein gespeichertes Gerät ist. Nicht alle gespeicherten Geräte werden authentifiziert.<br/> **Bthns \_ \_ \_ Geauthentifizierter Ergebnis Gerät** gibt an, dass das Gerät authentifiziert, gekoppelt oder gebunden ist. Alle authentifizierten Geräte werden gespeichert.<br/> |
| **lpszserviceingestancename** | Nicht verwendet.                                                                                                                                                                                                  | Anzeige Name des Geräts, das ursprünglich von einem Bluetooth-Remote namens Anforderungs Vorgang zurückgegeben und möglicherweise vom lokalen Benutzer aktualisiert wurde. Wird zurückgegeben, wenn der **\_ Rückgabe \_ Name** des PS angegeben ist                                                                                                                                                                                                                                         |
| **lpserviceclassid**        | Nicht verwendet.                                                                                                                                                                                                  | Das 32-Bit-Bluetooth-Klasse des Geräts (COD), das dem **data1** -Member der GUID zugeordnet ist. Wird zurückgegeben, wenn der **\_ Rückgabe- \_ Rückgabetyp**                                                                                                                                                                                                                                                                                    |
| **lpversion**               | Nicht verwendet.                                                                                                                                                                                                  | Nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszcomment**             | Nicht verwendet.                                                                                                                                                                                                  | Nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwnamespace**             | Muss NS- \_ BTH sein.                                                                                                                                                                                           | Gibt **NS- \_ BTH** zurück.                                                                                                                                                                                                                                                                                                                                                                                                            |
| **lpnsproviderid**          | Nicht verwendet.                                                                                                                                                                                                  | Nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszcontext**             | Nicht verwendet.                                                                                                                                                                                                  | Nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwnumofprotokolle**     | Nicht verwendet.                                                                                                                                                                                                  | Nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpafpprotokolle**          | Nicht verwendet.                                                                                                                                                                                                  | Nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszquerystring**         | Nicht verwendet.                                                                                                                                                                                                  | Nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwnumofcsaddrs**       | Nicht verwendet.                                                                                                                                                                                                  | Gibt die Anzahl der Elemente im Array der [**csaddr- \_ Informations**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info) Strukturen an.                                                                                                                                                                                                                                                                                                                          |
| **lpcsabuffer**             | Nicht verwendet.                                                                                                                                                                                                  | Zeiger auf eine [**csaddr- \_ Informations**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info) Struktur, deren **localaddr. lpsockaddr** -Member auf eine [**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) -Struktur mit der Adresse des Remote Geräts zeigt. Wird zurückgegeben, wenn die **\_ \_ addr-Rückgabe** Wert-Rückgabe angegeben                                                                                                                                                                  |
| **lpblob**                  | Dies ist optional. Kann auf eine [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) -Struktur verweisen, die auf eine [**BTH- \_ Abfrage \_ Geräte**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) Struktur zeigt, die die Länge der nicht zwischengespeicherten Geräte Abfrage Vorgänge einschränken kann. | Ein Zeiger auf eine [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) -Struktur, die auf eine [**BTH- \_ Geräte \_ Informations**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) Struktur zeigt. **lpblob** wird zurückgegeben, wenn das **\_ luprückgabeblob \_** angegeben wird. Geben Sie einen **luprückgabetamen \_ \_** zum Abrufen des Namens Felds der **BTH- \_ Geräte \_ Informationen** an.                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bluetooth und wsaqueryset für Set Service](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth und wsaqueryset für die Dienst Anfrage](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[Bluetooth und BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth und wsalookupservicebegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Bluetooth und WSALookupServiceNext](bluetooth-and-wsasetservice.md)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**Informationen zum BTH- \_ Gerät \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)
</dt> <dt>

[**BTH- \_ Abfrage \_ Gerät**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**csaddr- \_ Informationen**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**Wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

