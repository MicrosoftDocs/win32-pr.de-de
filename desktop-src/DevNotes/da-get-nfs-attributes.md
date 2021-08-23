---
description: Der DA \_ GET \_ NFS \_ ATTRIBUTES-Steuerungscode fragt zusätzliche Informationen zu einer NFS-Freigabe ab.
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: DA_GET_NFS_ATTRIBUTES-Steuerelementcode
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
ms.openlocfilehash: e3e2b974d58888c35c24e18f16e1e75da46a180bb8123e9745170e074cd448de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956109"
---
# <a name="da_get_nfs_attributes-control-code"></a>DA \_ GET \_ NFS \_ ATTRIBUTES-Steuerungscode

Der **DA \_ GET \_ NFS \_ ATTRIBUTES-Steuerungscode** fragt zusätzliche Informationen zu einer NFS-Freigabe ab.

Um diesen Vorgang durchzuführen, rufen Sie die [**Funktion DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern auf.


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

*hDevice* \[ In\]
</dt> <dd>

Ein Handle für eine Datei auf der NFS-Freigabe. Um dieses Handle zu erhalten, rufen Sie die [**CreateFile-Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) auf.

</dd> <dt>

*dwIoControlCode* \[ In\]
</dt> <dd>

Der Steuerungscode für den Vorgang. Verwenden **Sie DA GET \_ \_ NFS \_ ATTRIBUTES** für diesen Vorgang.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Wird mit diesem Vorgang nicht verwendet. auf **NULL festgelegt.**

</dd> <dt>

*nInBufferSize* \[ In\]
</dt> <dd>

Wird mit diesem Vorgang nicht verwendet. auf 0 (null) festgelegt.

</dd> <dt>

*lpOutBuffer* \[ out\]
</dt> <dd>

Ein Zeiger auf den Ausgabepuffer, der eine **NFS \_ FILE \_ ATTRIBUTES-Struktur** enthält. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*nOutBufferSize* \[ In\]
</dt> <dd>

Die Größe des Ausgabepuffers in Bytes.

</dd> <dt>

*lpBytesReturned* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten in Bytes empfängt.

Wenn der Ausgabepuffer zu klein ist, schlägt der Aufruf fehl, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt **ERROR INSUFFICIENT \_ \_ BUFFER** zurück, *und lpBytesReturned* ist 0 (null).

Wenn *lpOverlapped* **NULL ist,** *kann lpBytesReturned* nicht NULL **sein.** Auch wenn ein Vorgang keine Ausgabedaten zurückgibt und *lpOutBuffer* **NULL ist,** verwendet [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) *lpBytesReturned.* Nach einem solchen Vorgang ist der Wert *von lpBytesReturned* bedeutungslos.

Wenn *lpOverlapped* nicht **NULL ist,** *kann lpBytesReturned* NULL **sein.** Wenn dieser Parameter nicht **NULL ist** und der Vorgang Daten zurückgibt, *ist lpBytesReturned bedeutungslos,* bis der überlappende Vorgang abgeschlossen ist. Rufen Sie [**getOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult)auf, um die Anzahl der zurückgegebenen Bytes abzurufen. Wenn der *hDevice-Parameter* einem E/A-Abschlussport zugeordnet ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie [**GetQueuedCompletionStatus aufrufen.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**OVERLAPPED-Struktur.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)

Wenn *hDevice geöffnet wurde,* ohne **FILE FLAG \_ \_ OVERLAPPED** anzugeben, *wird lpOverlapped* ignoriert.

Wenn *hDevice mit* dem **FLAG FILE FLAG \_ \_ OVERLAPPED** geöffnet wurde, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt. In diesem Fall muss *lpOverlapped* auf eine gültige [**OVERLAPPED-Struktur**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) zeigen, die ein Handle für ein Ereignisobjekt enthält. Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.

Bei überlappenden Vorgängen [**gibt DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignisobjekt wird signalisiert, wenn der Vorgang abgeschlossen wurde. Andernfalls gibt die Funktion erst dann zurück, wenn der Vorgang abgeschlossen wurde oder ein Fehler auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wurde, [**gibt DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, [**gibt DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Diesem Steuerelementcode ist keine Headerdatei zugeordnet. Sie müssen den Steuerelementcode und die Datenstrukturen wie folgt definieren.

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

Die Strukturmitglieder können wie folgt beschrieben werden.

<dl> <dt>

<span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**
</dt> <dd>

Ein nicht transparenter Wert, der für spezielle Dateitypen wie Block-Special-, Character-Special- und FIFO-Dateien verwendet wird.

</dd> <dt>

<span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**
</dt> <dd>

Ein nicht transparenter Wert, der für spezielle Dateitypen wie Block-Special-, Character-Special- und FIFO-Dateien verwendet wird.

</dd> <dt>

<span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Sekunden**
</dt> <dd>

Ein 64-Bit-Wert, der die Sekunden seit dem 1. Januar 1970 (UTC) darstellt.

</dd> <dt>

<span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**
</dt> <dd>

Die Anzahl der Nanosekunden, die dem **Seconds-Member hinzugefügt werden** sollen.

</dd> <dt>

<span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**Filetype**
</dt> <dd>

Der NFS-Dateityp der Freigabe.



| NFS-Dateityp                                                                              | Beschreibung                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>NFS \_ TYPE \_ REG<br/>    | Eine reguläre Datei.<br/>           |
| <span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>NFS \_ TYPE \_ DIR<br/>    | Ein Verzeichnis.<br/>              |
| <span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>\_NFS-TYP \_ BLK<br/>    | Eine blockspezifische Datei.<br/>     |
| <span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>NFS \_ TYPE \_ CHR<br/>    | Eine zeichenspezifische Datei.<br/> |
| <span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>\_NFS-TYP \_ LNK<br/>    | Eine symbolische Verknüpfung.<br/>          |
| <span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>\_ \_ NFS-TYP-SOCK<br/> | Ein Windows Socket.<br/>         |
| <span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>\_NFS-TYP \_ FIFO<br/> | Eine FIFO-Datei.<br/>              |



 

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modus**
</dt> <dd>

Der Dateimodus.

</dd> <dt>

<span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**
</dt> <dd>

Die Anzahl der Links zur Freigabe.

</dd> <dt>

<span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Uid**
</dt> <dd>

Die UNIX Benutzer-ID (UID).

</dd> <dt>

<span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Gid**
</dt> <dd>

Der UNIX Gruppenbezeichner (GID).

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Größe**
</dt> <dd>

Die Dateigröße in Bytes.

</dd> <dt>

<span id="Used"></span><span id="used"></span><span id="USED"></span>**gebraucht**
</dt> <dd>

Die verwendete Dateigröße in Bytes. Dies ist identisch mit der Dateigröße.

</dd> <dt>

<span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**
</dt> <dd>

Die Geräte-ID.

</dd> <dt>

<span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**
</dt> <dd>

Der Dateisystembezeichner.

</dd> <dt>

<span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileId**
</dt> <dd>

Der Dateibezeichner.

</dd> <dt>

<span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**
</dt> <dd>

Der Zeitpunkt des letzten Zugriffs.

</dd> <dt>

<span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**
</dt> <dd>

Der Zeitpunkt der letzten Änderung.

</dd> <dt>

<span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**
</dt> <dd>

Der Zeitpunkt der letzten Änderung.

</dd> <dt>

<span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**Fileattributes**
</dt> <dd>

Eine **NFS \_ FILE \_ ATTRIBUTES-Struktur.**

> [!Note]  
> Ausführlichere Beschreibungen der Member dieser Struktur finden Sie in der **FATTR3-Struktur** in der NFS-Protokollspezifikation Version 3 (wie in [RFC 1813 definiert).](https://www.ietf.org/rfc/rfc1813.txt)

 

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**
</dt> <dd>

Gibt an, ob die Verbindung, über die das Handle zur NFS-Freigabe erstellt wurde, über das NFS-Protokoll Version 2 oder NFS Version 3 erfolgt.



| Wert                            | Beschreibung              |
|----------------------------------|--------------------------|
| <span id="2"></span>2<br/> | NFS Version 2<br/> |
| <span id="3"></span>3<br/> | NFS Version 3<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>    |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>         |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Deviceiocontrol**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
