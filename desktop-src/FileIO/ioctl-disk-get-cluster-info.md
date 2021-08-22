---
description: Ruft die Attribute des angegebenen Datenträgergeräts ab.
ms.assetid: 2FF81F67-9E70-43C6-A504-0D60382E0945
title: IOCTL_DISK_GET_CLUSTER_INFO -Steuerelementcode (Ntdddisk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_GET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 3acf923a9f0288bd3fe3a0b12d4c61b71437f61c1c4f96a3a3bef1af5f05fd95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068680"
---
# <a name="ioctl_disk_get_cluster_info-control-code"></a>IOCTL \_ DISK GET CLUSTER \_ \_ \_ INFO-Steuerungscode

Ruft die Attribute des angegebenen Datenträgergeräts ab.

Um diesen Vorgang durchzuführen, rufen Sie die [**Funktion DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern auf.


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_GET_CLUSTER_INFO,    // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Ein Handle für den Datenträger.

Um ein Gerätehand handle abzurufen, rufen Sie die [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) auf.

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Der Steuerungscode für den Vorgang.

Verwenden **Sie IOCTL \_ DISK GET CLUSTER \_ \_ \_ INFO** für diesen Vorgang.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Wird mit diesem Vorgang nicht verwendet. Legen Sie auf **NULL fest.**

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Die Größe des Eingabepuffers in Bytes. Legen Sie auf 0 (null) fest.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine [**DISK \_ CLUSTER \_ INFO-Datenstruktur**](disk-cluster-info.md) empfängt.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Die Größe des Ausgabepuffers in Bytes.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Wird mit diesem Vorgang nicht verwendet. Legen Sie auf **NULL fest.**

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Ein Zeiger auf eine [**OVERLAPPED-Struktur.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Wenn *hDevice geöffnet wurde,* ohne **FILE FLAG \_ \_ OVERLAPPED** anzugeben, *wird lpOverlapped* ignoriert.

Wenn *hDevice mit* dem **FLAG FILE FLAG \_ \_ OVERLAPPED** geöffnet wurde, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt. In diesem Fall muss *lpOverlapped* auf eine gültige [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) zeigen, die ein Handle für ein Ereignisobjekt enthält. Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.

Bei überlappenden Vorgängen [**gibt DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignisobjekt wird signalisiert, wenn der Vorgang abgeschlossen wurde. Andernfalls gibt die Funktion erst dann zurück, wenn der Vorgang abgeschlossen wurde oder ein Fehler auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wurde und angibt, dass alle Volumes auf dem Datenträger einsatzbereit sind, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, [**gibt DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntdddisk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Steuerungscodes für die Datenträgerverwaltung](disk-management-control-codes.md)
</dt> <dt>

[**\_ \_ DATENTRÄGERCLUSTERINFORMATIONEN**](disk-cluster-info.md)
</dt> <dt>

[**IOCTL \_ DISK \_ SET \_ CLUSTER \_ INFO**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

