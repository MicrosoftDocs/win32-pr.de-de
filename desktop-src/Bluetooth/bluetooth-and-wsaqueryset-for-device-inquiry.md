---
title: Bluetooth und WSAQUERYSET für Geräteabfragen
description: Wird verwendet, um die Ermittlung von Geräten und Diensten im Bluetooth Namespace NS BTH zu \_ erleichtern.
ms.assetid: 0c0d26f7-b6c3-42a9-8c01-118278c381cc
keywords:
- Bluetooth und WSAQUERYSET für Bluetooth
- WSAQUERYSET Bluetooth für Geräteabfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a9250670fda52f2ecdc27ffee949b12049b8ec2860b7ee2df23631c4469076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959279"
---
# <a name="bluetooth-and-wsaqueryset-for-device-inquiry"></a>Bluetooth und WSAQUERYSET für Geräteabfragen

In Bluetooth wird die [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) verwendet, um die Ermittlung von Geräten und Diensten im Bluetooth Namespace NS BTH zu \_ erleichtern.

Die Funktionen [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) und [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) verwenden die [**WSAQUERYSET-Struktur,**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) um Informationen zum Geräteabfrageprozess abzurufen. In der folgenden Tabelle werden Memberwerte in der **WSAQUERYSET-Struktur** aufgelistet und beschrieben.

| Member                      | Eingabe in WSALookupServiceBegin mit \_ angegebenen LUP-CONTAINERn                                                                                                                                              | Rückgabewert von WSALookupServiceNext                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**                  | Muss auf **sizeof** festgelegt werden ([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                       | **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)) wird vom System zurückgegeben.                                                                                                                                                                                                                                                                                                                                                        |
| **dwOutputFlags**           | Wird nicht verwendet.                                                                                                                                                                                                  | Möglicherweise ist mindestens eines dieser Flags festgelegt: **BTHNS \_ RESULT \_ DEVICE \_ CONNECTED** Gibt an, dass das Gerät verbunden ist.<br/> **BTHNS \_ RESULT \_ DEVICE \_ REMEMBERED** Gibt an, dass das Gerät ein gespeichertes Gerät ist. Nicht alle gespeicherten Geräte werden authentifiziert.<br/> **BTHNS \_ RESULT \_ DEVICE \_ AUTHENTICATED** Gibt an, dass das Gerät authentifiziert, gekoppelt oder gebunden ist. Alle authentifizierten Geräte werden gespeichert.<br/> |
| **lpszServiceInstanceName** | Wird nicht verwendet.                                                                                                                                                                                                  | Anzeigename des Geräts, ursprünglich von einem Bluetooth Remotenamenanforderungsvorgang zurückgegeben und möglicherweise vom lokalen Benutzer aktualisiert. Wird zurückgegeben, wenn **LUP \_ RETURN \_ NAME** angegeben ist.                                                                                                                                                                                                                                         |
| **lpServiceClassId**        | Wird nicht verwendet.                                                                                                                                                                                                  | Die 32-Bit-Bluetooth Klasse des Gerätefelds (COD), das dem **Data1-Member** der GUID zugeordnet ist. Wird zurückgegeben, wenn **LUP \_ RETURN \_ TYPE** angegeben ist.                                                                                                                                                                                                                                                                                    |
| **lpVersion**               | Nicht verwendet.                                                                                                                                                                                                  | Nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszComment**             | Nicht verwendet.                                                                                                                                                                                                  | Nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNameSpace**             | Muss NS \_ BTH sein.                                                                                                                                                                                           | Gibt **NS \_ BTH** zurück.                                                                                                                                                                                                                                                                                                                                                                                                            |
| **lpNSProviderId**          | Nicht verwendet.                                                                                                                                                                                                  | Nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszContext**             | Nicht verwendet.                                                                                                                                                                                                  | Nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfProtocols**     | Nicht verwendet.                                                                                                                                                                                                  | Nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpafpProtocols**          | Nicht verwendet.                                                                                                                                                                                                  | Nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszQueryString**         | Nicht verwendet.                                                                                                                                                                                                  | Nicht verwendet.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfCsAddrs**       | Wird nicht verwendet.                                                                                                                                                                                                  | Gibt die Anzahl der Elemente im Array der [**CSADDR \_ INFO-Strukturen**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info) an.                                                                                                                                                                                                                                                                                                                          |
| **lpcsaBuffer**             | Wird nicht verwendet.                                                                                                                                                                                                  | Zeiger auf eine [**CSADDR \_ INFO-Struktur**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info) mit ihrem **LocalAddr.lpSockaddr-Member,** der auf eine [**SOCKADDR-BTH-Struktur \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) mit der Adresse des Remotegeräts zeigt. Wird zurückgegeben, wenn **LUP \_ RETURN \_ ADDR** angegeben ist.                                                                                                                                                                  |
| **lpBlob**                  | Optional. Kann auf eine [**BLOB-Struktur**](/windows/desktop/api/nspapi/ns-nspapi-blob) verweisen, die auf eine [**BTH \_ QUERY \_ DEVICE-Struktur**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) verweist, die die Länge nicht zwischengespeicherter Geräteabfragevorgänge einschränken kann. | Zeiger auf eine [**BLOB-Struktur,**](/windows/desktop/api/nspapi/ns-nspapi-blob) die auf eine [**BTH \_ DEVICE \_ INFO-Struktur**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) zeigt. **lpBlob** wird zurückgegeben, wenn **LUP \_ RETURN \_ BLOB** angegeben ist. Geben Sie **LUP \_ RETURN \_ NAME** an, um das Namensfeld von **BTH \_ DEVICE \_ INFO** abzurufen.                                                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bluetooth und WSAQUERYSET für Set Service](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth und WSAQUERYSET für Dienstabfragen](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[Bluetooth und BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth und WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Bluetooth und WSALookupServiceNext](bluetooth-and-wsasetservice.md)
</dt> <dt>

[**Blob**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_BTH-GERÄTEINFORMATIONEN \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)
</dt> <dt>

[**\_BTH-ABFRAGEGERÄT \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**CSADDR \_ INFO**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

