---
description: Der "da \_ Get NFS-Attribute"- \_ \_ Steuerungs Code fragt zusätzliche Informationen über eine NFS-Freigabe ab.
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: DA_GET_NFS_ATTRIBUTES Steuerungs Codes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DA_GET_NFS_ATTRIBUTES
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4427dd48190bd12f7837c4841a98e15f7ddaff5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523371"
---
# <a name="da_get_nfs_attributes-control-code"></a>Steuerelement Code für da \_ Get NFS- \_ \_ Attribute

Der " **da \_ Get NFS- \_ \_ Attribute** "-Steuerungs Code fragt zusätzliche Informationen über eine NFS-Freigabe ab.

Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.


```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,               // handle to device
                    (DWORD)        DA_GET_NFS_ATTRIBUTES, // dwIoControlCode
                                   NULL,                  // lpInBuffer
                                   0,                     // nInBufferSize
                    (LPDWORD)      lpOutBuffer,           // output buffer
                    (DWORD)        nOutBufferSize,        // size of output buffer
                    (LPDWORD)      lpBytesReturned,       // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* \[ in\]
</dt> <dd>

Ein Handle für eine Datei auf der NFS-Freigabe. Um dieses Handle zu erhalten, rufen [**Sie die Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.

</dd> <dt>

*dwIoControlCode* \[ in\]
</dt> <dd>

Der Steuerelement Code für den Vorgang. Verwenden Sie für diesen Vorgang " **da \_ get \_ NFS \_** "-Attribute.

</dd> <dt>

*lpinbuffer* 
</dt> <dd>

Wird bei diesem Vorgang nicht verwendet. auf **null** festgelegt.

</dd> <dt>

*nInBufferSize* \[ in\]
</dt> <dd>

Wird bei diesem Vorgang nicht verwendet. auf NULL festgelegt.

</dd> <dt>

*lpoutbuffer* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den Ausgabepuffer, der eine **NFS- \_ Datei \_ Attribute** -Struktur enthält. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*nOutBufferSize* \[ in\]
</dt> <dd>

Die Größe des Ausgabepuffers in Bytes.

</dd> <dt>

*lpbyteszurück gegeben* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.

Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen **fehlerhaften \_ \_ Puffer** zurück, und *lpbytesreturns* ist 0 (null).

Wenn *lpoverllapp* den **Wert NULL** hat, kann *lpbytes-Rückgabe* Wert nicht **null** sein. Selbst wenn ein Vorgang keine Ausgabedaten zurückgibt und *lpoutbuffer* den Wert **null** hat, verwendet [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) *lpbytesreturn*. Nach einem solchen Vorgang ist der Wert von *lpbytesno* bedeutungslos.

Wenn *lpoverllapp* nicht **null** ist, kann *lpbytesgab* **null** sein. Wenn dieser Parameter nicht **null** ist und der Vorgang Daten zurückgibt, ist *lpbytesreturns* bedeutungslos, bis der überlappende Vorgang abgeschlossen ist. Um die Anzahl der zurückgegebenen Bytes abzurufen, rufen Sie [**gezu verlappedresult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult)auf. Wenn der *hdevice* -Parameter einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)aufrufen.

</dd> <dt>

*lpoverlgetauscht* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.

Wenn *hdevice* ohne Angabe eines überlappenden **\_ Dateiflags \_** geöffnet wurde, wird *lpoverlgetauscht* ignoriert.

Wenn *hdevice* mit dem überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt. In diesem Fall muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur verweisen, die ein Handle für ein Ereignis Objekt enthält. Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.

Bei überlappenden Vorgängen gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignis Objekt wird signalisiert, wenn der Vorgang abgeschlossen wurde. Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Diesem Steuerungs Code ist keine Header Datei zugeordnet. Sie müssen den Steuerungs Code und die Datenstrukturen wie folgt definieren.

``` syntax
#define DEVICE_DA_RDR 0x80000  
 
#define DA_GET_NFS_ATTRIBUTES CTL_CODE(DEVICE_DA_RDR, 0x804, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _NFS_SPEC_DATA {  
    ULONG               SpecData1;
    ULONG               SpecData2;
} NFS_SPEC_DATA, *PNFS_SPEC_DATA;

typedef struct _NFS_TIME {
    ULONG        Seconds;
    ULONG        nSeconds;
} NFS_TIME, *PNFS_TIME;

#define NFS_TYPE_REG         1
#define NFS_TYPE_DIR         2
#define NFS_TYPE_BLK         3
#define NFS_TYPE_CHR         4
#define NFS_TYPE_LNK         5
#define NFS_TYPE_SOCK        6
#define NFS_TYPE_FIFO        7

typedef struct _NFS_FILE_ATTRIBUTES {  
    ULONG               FileType;  
    ULONG               Mode;  
    ULONG               NLink;  
    ULONG               Uid;  
    ULONG               Gid;  
    ULONGLONG           Size;  
    ULONGLONG           Used;
    NFS_SPEC_DATA       Rdev;
    ULONGLONG           Fsid;  
    ULONGLONG           FileId;  
    NFS_TIME            AccessTime;  
    NFS_TIME            ModifyTime;  
    NFS_TIME            ChangeTime;  
} NFS_FILE_ATTRIBUTES, *PNFS_FILE_ATTRIBUTES;

typedef struct _DA_FILE_ATTRIBUTES {  
    NFS_FILE_ATTRIBUTES FileAttributes;  
    ULONG               Version;  
} DA_FILE_ATTRIBUTES, *PDA_FILE_ATTRIBUTES;
```

Die Strukturmember können wie folgt beschrieben werden.

<dl> <dt>

<span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**
</dt> <dd>

Ein nicht transparenter Wert, der für spezielle Dateitypen wie z. b. Block-Special-, Character-Special-und FIFO-Dateien verwendet wird.

</dd> <dt>

<span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**
</dt> <dd>

Ein nicht transparenter Wert, der für spezielle Dateitypen wie z. b. Block-Special-, Character-Special-und FIFO-Dateien verwendet wird.

</dd> <dt>

<span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Vorsprung**
</dt> <dd>

Ein 64-Bit-Wert, der die Sekunden seit dem 1. Januar 1970 (UTC) darstellt.

</dd> <dt>

<span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSekunden**
</dt> <dd>

Die Anzahl der Nanosekunden, die dem **Sekunden** -Element hinzugefügt werden sollen.

</dd> <dt>

<span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**
</dt> <dd>

Der NFS-Dateityp der Freigabe.



| NFS-Dateityp                                                                              | BESCHREIBUNG                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>NFS- \_ Typ- \_ reg<br/>    | Eine reguläre Datei.<br/>           |
| <span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>NFS- \_ typverzeichnis \_<br/>    | Ein Verzeichnis.<br/>              |
| <span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>NFS- \_ Typ \_ BLK<br/>    | Eine Block spezifische Datei.<br/>     |
| <span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>NFS- \_ Typ \_ Chr<br/>    | Eine Zeichen spezifische Datei.<br/> |
| <span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>NFS- \_ Typ \_ lnk<br/>    | Eine symbolische Verknüpfung.<br/>          |
| <span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>NFS- \_ Typ- \_ Sock<br/> | Ein Windows-Socket.<br/>         |
| <span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>NFS- \_ Typ \_ FIFO<br/> | Eine FIFO-Datei.<br/>              |



 

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Spar**
</dt> <dd>

Der Dateimodus.

</dd> <dt>

<span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**Nlink**
</dt> <dd>

Die Anzahl der Links zur Freigabe.

</dd> <dt>

<span id="Uid"></span><span id="uid"></span><span id="UID"></span>**UID**
</dt> <dd>

Die UNIX-Benutzer-ID (UID).

</dd> <dt>

<span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Ü**
</dt> <dd>

Der UNIX-Gruppen Bezeichner (GID).

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Größe**
</dt> <dd>

Die Dateigröße in Bytes.

</dd> <dt>

<span id="Used"></span><span id="used"></span><span id="USED"></span>**Daran**
</dt> <dd>

Die verwendete Dateigröße in Bytes. Dies entspricht der Dateigröße.

</dd> <dt>

<span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**
</dt> <dd>

Der Geräte Bezeichner.

</dd> <dt>

<span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**-Sid**
</dt> <dd>

Der Bezeichner des Dateisystems.

</dd> <dt>

<span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileID**
</dt> <dd>

Der Dateibezeichner.

</dd> <dt>

<span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**ACCESSTIME**
</dt> <dd>

Der Zeitpunkt des letzten Zugriffs.

</dd> <dt>

<span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**Modifytime**
</dt> <dd>

Der Zeitpunkt der letzten Änderung.

</dd> <dt>

<span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**Changetime**
</dt> <dd>

Der Zeitpunkt der letzten Änderung.

</dd> <dt>

<span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**File Attributes**
</dt> <dd>

Eine **NFS- \_ Datei \_ Attribute** -Struktur.

> [!Note]  
> Ausführlichere Beschreibungen der Member dieser Struktur finden Sie in der **fattr3** -Struktur in der Version 3 des NFS-Protokolls (wie in [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)definiert).

 

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**
</dt> <dd>

Gibt an, ob die Verbindung, auf der das Handle für die NFS-Freigabe erstellt wurde, über NFS Version 2 oder das NFS-Protokoll (Version 3) erfolgt.



| Wert                            | BESCHREIBUNG              |
|----------------------------------|--------------------------|
| <span id="2"></span>2<br/> | NFS Version 2<br/> |
| <span id="3"></span>€<br/> | NFS Version 3<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>    |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>         |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
