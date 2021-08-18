---
title: GUESTOSVERSIONINFOEX-Struktur (VPCCOMInterfaces.h)
description: Enthält Informationen zur Betriebssystemversion für das Gastbetriebssystem.
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- GUESTOSVERSIONINFOEX-Struktur Virtueller PC
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
ms.openlocfilehash: 848196448c2bd6f021d85f7c13972e81664dd60a0e4a0bbbd2e05ef3455aade7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056908"
---
# <a name="guestosversioninfoex-structure"></a>GUESTOSVERSIONINFOEX-Struktur

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Enthält Informationen zur Betriebssystemversion für das Gastbetriebssystem.

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

Die Größe dieser Datenstruktur in Bytes. Legen Sie diesen Member auf `sizeof(GUESTOSVERSIONINFOEX)` fest.

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

Die Betriebssystemplattform. Dieser Member kann **VER \_ PLATFORM \_ WIN32 \_ NT** (2) sein.

</dd> <dt>

**szCSDVersion**
</dt> <dd>

Eine auf NULL beendete Zeichenfolge, z. B. "Service Pack 3", die das neueste auf dem System installierte Service Pack angibt. Wenn kein Service Pack installiert wurde, ist die Zeichenfolge leer.

</dd> <dt>

**wServicePackMajor**
</dt> <dd>

Die Hauptversionsnummer des neuesten installierten Service Packs.

</dd> <dt>

**wServicePackMinor**
</dt> <dd>

Die Nebenversionsnummer des neuesten installierten Service Packs.

</dd> <dt>

**wSuiteMask**
</dt> <dd>

Eine Bitmaske, die die im System verfügbaren Produktsammlungen identifiziert. Dieser Member kann eine Kombination der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <dt>**VER \_ SUITE \_ BACKOFFICE**</dt> <dt>0x00000004</dt> </dl>                                            | Microsoft BackOffice-Komponenten werden installiert.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <dt>**VER \_ \_BLATT"-0X00000400**</dt> <dt></dt> </dl>                                                           | Windows Server 2003, Web Edition ist installiert.<br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <dt>**VER \_ SUITE \_ COMPUTE \_ SERVER**</dt> <dt>0x00004000</dt> </dl>                               | Windows Server 2003, Compute Cluster Edition ist installiert.<br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <dt>**VER \_ SUITE \_ DATACENTER**</dt> <dt>0X00000080</dt> </dl>                                            | Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition oder Windows 2000 Datacenter Server ist installiert.<br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <dt>**VER \_ SUITE \_ ENTERPRISE**</dt> <dt>0x00000002</dt> </dl>                                            | Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition oder Windows 2000 Advanced Server ist installiert. Weitere Informationen zu diesem Bitflag finden Sie im Abschnitt "Hinweise".<br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <dt>**VER \_ SUITE \_ EMBEDDEDNT**</dt> <dt>0x00000040</dt> </dl>                                            | Windows XP Embedded ist installiert.<br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <dt>**VER \_ SUITE \_ PERSONAL**</dt> <dt>0X00000200</dt> </dl>                                                  | Windows Vista Home Premium, Windows Vista Home Basic oder Windows XP Home Edition ist installiert.<br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <dt>**VER \_ SUITE \_ SINGLEUSERTS**</dt> <dt>0x00000100</dt> </dl>                                      | Remotedesktop wird unterstützt, aber nur eine interaktive Sitzung wird unterstützt. Dieser Wert wird festgelegt, es sei denn, das System wird im Anwendungsservermodus ausgeführt.<br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <dt>**VER \_ SUITE \_ SMALLBUSINESS**</dt> <dt>0x00000001</dt> </dl>                                   | Microsoft Small Business Server wurde einmal auf dem System installiert, wurde aber möglicherweise auf eine andere Version von Windows. Weitere Informationen zu diesem Bitflag finden Sie im Abschnitt "Hinweise".<br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <dt>**VER \_ SUITE \_ SMALLBUSINESS \_ RESTRICTED**</dt> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server wird mit der restriktiven Clientlizenz installiert. Weitere Informationen zu diesem Bitflag finden Sie im Abschnitt "Hinweise".<br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <dt>**VER \_ SUITE \_ STORAGE \_ SERVER**</dt> <dt>0x00002000</dt> </dl>                               | Windows Storage Server 2003 R2 oder Windows Storage Server 2003 ist installiert.<br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <dt>**VER \_ SUITE \_ TERMINAL**</dt> <dt>0x00000010</dt> </dl>                                                  | Terminaldienste sind installiert. Dieser Wert wird immer festgelegt.<br/> Wenn **VER SUITE TERMINAL \_ \_ festgelegt** ist, **ABER VER SUITE \_ \_ SINGLEUSERTS** nicht festgelegt ist, wird das System im Anwendungsservermodus ausgeführt.<br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <dt>**VER \_ SUITE \_ WH \_ SERVER**</dt> <dt>0x00008000</dt> </dl>                                              | Windows Home Server ist installiert.<br/>                                                                                                                                                                      |



 

</dd> <dt>

**wProductType**
</dt> <dd>

Alle zusätzlichen Informationen zum System. Dieser Member kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <dt>**VER \_ \_ \_ NT-DOMÄNENCONTROLLER-0x0000002**</dt> <dt></dt> </dl> | Das System ist ein Domänencontroller, und das Betriebssystem ist Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 oder Windows 2000 Server.<br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <dt>**VER \_ NT \_ SERVER**</dt> <dt>0x0000003</dt> </dl>                                   | Das Betriebssystem ist Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 oder Windows 2000 Server.<br/> Beachten Sie, dass ein Server, der auch ein Domänencontroller ist, als **VER \_ NT DOMAIN \_ \_ CONTROLLER** und nicht **als VER NT SERVER gemeldet \_ \_ wird.**<br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <dt>**VER \_ NT \_ WORKSTATION**</dt> <dt>0x0000001</dt> </dl>                    | Das Betriebssystem ist Windows 7, Windows Vista, Windows XP oder Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**wReserved**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMGuestOS::GetOsVersionInfo**](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

