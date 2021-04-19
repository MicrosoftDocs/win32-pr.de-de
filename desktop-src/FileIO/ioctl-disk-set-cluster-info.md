---
description: Legt die Cluster Informationen auf einem Datenträger fest.
ms.assetid: AB2243D9-4913-4412-87E0-2C8DB8AB10B8
title: IOCTL_DISK_SET_CLUSTER_INFO Steuerungs Code (ntdddisk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_SET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 4ba0994dd1c9030e84c22e24b1eb4583eba7e3d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363720"
---
# <a name="ioctl_disk_set_cluster_info-control-code"></a>Ioctl-Datenträger \_ \_ Satz- \_ \_ Informations Steuerungs Code für Cluster

Legt die Cluster Informationen auf einem Datenträger fest.

Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_SET_CLUSTER_INFO,    // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Ein Handle für den Datenträger.

Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) "-Funktion" auf.

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Der Steuerelement Code für den Vorgang.

Verwenden Sie für diesen Vorgang die **\_ \_ \_ Cluster \_ Informationen für die IOCTL-Festplatte** .

</dd> <dt>

*lpinbuffer* 
</dt> <dd>

Ein Zeiger auf eine Datenträger [**\_ Cluster \_ Info**](disk-cluster-info.md) -Datenstruktur, die Cluster Informationen für den Datenträger enthält.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Die Größe des Eingabe Puffers in Bytes.

</dd> <dt>

*lpoutbuffer* 
</dt> <dd>

Wird bei diesem Vorgang nicht verwendet. Auf **null** festgelegt.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Die Größe des Ausgabepuffers in Bytes. Legen Sie den Wert auf 0 (null) fest.

</dd> <dt>

*lpbyteszurück gegeben* 
</dt> <dd>

Wird bei diesem Vorgang nicht verwendet. Auf **null** festgelegt.

</dd> <dt>

*lpoverlgetauscht* 
</dt> <dd>

Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.

Wenn *hdevice* ohne Angabe eines überlappenden **\_ Dateiflags \_** geöffnet wurde, wird *lpoverlgetauscht* ignoriert.

Wenn *hdevice* mit dem überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt. In diesem Fall muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur verweisen, die ein Handle für ein Ereignis Objekt enthält. Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.

Bei überlappenden Vorgängen gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignis Objekt wird signalisiert, wenn der Vorgang abgeschlossen wurde. Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wurde, was darauf hinweist, dass alle Volumes auf dem Datenträger einsatzbereit sind, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntdddisk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Steuerungs Codes für die Datenträgerverwaltung](disk-management-control-codes.md)
</dt> <dt>

[**Informationen zum Datenträger \_ Cluster \_**](disk-cluster-info.md)
</dt> <dt>

[**ioctl-Datenträger \_ \_ get \_ Cluster \_ Info**](ioctl-disk-get-cluster-info.md)
</dt> </dl>

 

