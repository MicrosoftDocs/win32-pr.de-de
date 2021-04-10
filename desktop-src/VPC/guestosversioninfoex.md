---
title: Guestosversioninfoex-Struktur (vpccominterfaces. h)
description: Enthält Informationen zur Betriebssystemversion für das Gast Betriebssystem.
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- Guestosversioninfoex-Struktur virtueller PC
topic_type:
- apiref
api_name:
- GUESTOSVERSIONINFOEX
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633838affb9a9ff1453a0c49de9588428b038fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104277"
---
# <a name="guestosversioninfoex-structure"></a>Guestosversioninfoex-Struktur

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Enthält Informationen zur Betriebssystemversion für das Gast Betriebssystem.

## <a name="syntax"></a>Syntax


```C++
typedef struct _GUESTOSVERSIONINFOEX {
  long    dwOSVersionInfoSize;
  long    dwMajorVersion;
  long    dwMinorVersion;
  long    dwBuildNumber;
  long    dwPlatformId;
  wchar_t szCSDVersion[128];
  short   wServicePackMajor;
  short   wServicePackMinor;
  short   wSuiteMask;
  byte    wProductType;
  byte    wReserved;
} GUESTOSVERSIONINFOEX;
```



## <a name="members"></a>Member

<dl> <dt>

**dwOSVersionInfoSize**
</dt> <dd>

Die Größe dieser Datenstruktur in Bytes. Legen Sie diesen Member auf fest `sizeof(GUESTOSVERSIONINFOEX)` .

</dd> <dt>

**dwMajorVersion**
</dt> <dd>

Die Hauptversionsnummer.

</dd> <dt>

**dwMinorVersion**
</dt> <dd>

Die Nebenversionsnummer.

</dd> <dt>

**dwBuildNumber**
</dt> <dd>

Die Buildnummer.

</dd> <dt>

**dwPlatformId**
</dt> <dd>

Die Betriebssystem Plattform. Dieser Member kann ein " **ver \_ Platform \_ Win32 \_ NT** " (2) sein.

</dd> <dt>

**szCSDVersion**
</dt> <dd>

Eine mit NULL endenden Zeichenfolge, z. b. "Service Pack 3", die das neueste Service Pack angibt, das auf dem System installiert ist. Wenn kein Service Pack installiert wurde, ist die Zeichenfolge leer.

</dd> <dt>

**wServicePackMajor**
</dt> <dd>

Die Hauptversionsnummer des neuesten installierten Service Packs.

</dd> <dt>

**wServicePackMinor**
</dt> <dd>

Die neben Versionsnummer des neuesten installierten Service Packs.

</dd> <dt>

**wSuiteMask**
</dt> <dd>

Eine Bitmaske, die die im System verfügbaren Produkt Suites identifiziert. Dieser Member kann eine Kombination der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <dt>**Ver \_ Suite \_ BackOffice**</dt> <dt>0x00000004</dt> </dl>                                            | Microsoft BackOffice-Komponenten werden installiert.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <dt>**Ver \_ \_Blatt "Sammlung**</dt> " <dt>0x00000400</dt> </dl>                                                           | Windows Server 2003, Web Edition ist installiert.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <dt>**Ver \_ Suite \_ Compute \_ Server**</dt> <dt>0x00004000</dt> </dl>                               | Windows Server 2003, Compute Cluster Edition ist installiert.<br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <dt>**Ver \_ Suite \_ Datacenter**</dt> <dt>0x00000080</dt> </dl>                                            | Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition oder Windows 2000 Datacenter Server ist installiert.<br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <dt>**Ver \_ Suite \_ Enterprise**</dt> <dt>0x00000002</dt> </dl>                                            | Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition oder Windows 2000 Advanced Server ist installiert. Weitere Informationen zu diesem Bitflag finden Sie im Abschnitt "Hinweise".<br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <dt>**Ver \_ Suite \_ embeddnt**</dt> <dt>0x00000040</dt> </dl>                                            | Windows XP Embedded ist installiert.<br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <dt>**Ver \_ Suite \_ Personal**</dt> <dt>0x00000200</dt> </dl>                                                  | Windows Vista Home Premium, Windows Vista Home Basic oder Windows XP Home Edition ist installiert.<br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <dt>**Ver \_ Suite \_ singleuserts**</dt> <dt>0x00000100</dt> </dl>                                      | Remotedesktop wird unterstützt, es wird jedoch nur eine interaktive Sitzung unterstützt. Dieser Wert wird festgelegt, es sei denn, das System wird im Anwendungsserver Modus ausgeführt.<br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <dt>**Ver \_ Suite \_ SmallBusiness**</dt> <dt>0x00000001</dt> </dl>                                   | Microsoft Small Business Server wurde auf dem System installiert, kann jedoch auf eine andere Version von Windows aktualisiert werden. Weitere Informationen zu diesem Bitflag finden Sie im Abschnitt "Hinweise".<br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <dt>**Ver \_ \_SmallBusiness \_ restricted Suite**</dt> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server wird mit der eingeschränkten Client Lizenz in Kraft installiert. Weitere Informationen zu diesem Bitflag finden Sie im Abschnitt "Hinweise".<br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <dt>**Ver \_ Suite \_ Storage \_ Server**</dt> <dt>0x00002000</dt> </dl>                               | Windows Storage Server 2003 R2 oder Windows Storage Server 2003ist installiert.<br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <dt>**Ver \_ Suite- \_ Terminal**</dt> <dt>0x00000010</dt> </dl>                                                  | Terminal Dienste sind installiert. Dieser Wert ist immer festgelegt.<br/> Wenn das **ver \_ Suite- \_ Terminal** festgelegt ist, aber **ver \_ Suite \_ singleuserts** nicht festgelegt ist, wird das System im Anwendungsserver Modus ausgeführt.<br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <dt>**Ver \_ Suite- \_ WH- \_ Server**</dt> <dt>0x00008000</dt> </dl>                                              | Windows Home Server ist installiert.<br/>                                                                                                                                                                      |



 

</dd> <dt>

**wProductType**
</dt> <dd>

Weitere Informationen zum System. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <dt>**Ver \_ NT- \_ Domänen \_ Controller**</dt> <dt>0x0000002</dt> </dl> | Das System ist ein Domänen Controller, und das Betriebssystem ist Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 oder Windows 2000 Server.<br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <dt>**Ver \_ NT \_ Server**</dt> <dt>0x0000003</dt> </dl>                                   | Das Betriebssystem ist Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 oder Windows 2000 Server.<br/> Beachten Sie, dass ein Server, der auch ein Domänen Controller ist, als **ver- \_ NT- \_ Domänen \_ Controller**, nicht als **ver-NT- \_ \_ Server** gemeldet<br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <dt>**Ver \_ NT- \_ Arbeits**</dt> Station <dt>0x0000001</dt> </dl>                    | Das Betriebssystem ist Windows 7, Windows Vista, Windows XP oder Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**wReserved**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmguestos:: getosversioninfo**](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

