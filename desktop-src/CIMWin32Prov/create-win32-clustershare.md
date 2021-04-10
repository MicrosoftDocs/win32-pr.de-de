---
description: Erstellt eine neue Win32- \_ clustershare-Instanz.
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Create-Methode der Win32_ClusterShare-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cbf7c42b8523bcd12b19e9b474ecc50bd031939
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127649"
---
# <a name="create-method-of-the-win32_clustershare-class"></a>Create-Methode der Win32 \_ clustershare-Klasse

Erstellt eine neue [**Win32- \_ clustershare**](win32-clustershare.md) -Instanz.

## <a name="syntax"></a>Syntax


```mof
static uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* \[ in\]
</dt> <dd>

Lokaler Pfad der Windows-Freigabe.

Beispiel: "C: \\ Program Files".

</dd> <dt>

*Name* \[ in\]
</dt> <dd>

Der Alias für einen Pfad, der als Freigabe auf einem Computersystem eingerichtet wird, auf dem Windows ausgeführt wird.

Beispiel: "Public".

</dd> <dt>

*Typ* \[ in\]
</dt> <dd>

Der Typ der freigegebenen Ressource. Zu den Typen zählen: Laufwerke, Druck Warteschlangen, prozessübergreifende Kommunikation (prozessübergreifende Communications, IPC) und allgemeine Geräte.

<dt>

0 (0x0)
</dt> <dd>

Laufwerk

</dd> <dt>

1 (0x1)
</dt> <dd>

Druckwarteschlange

</dd> <dt>

2 (0x2)
</dt> <dd>

Sicherungsmedium

</dd> <dt>

3 (0x3)
</dt> <dd>

IPC

</dd> <dt>

2147483648 (0x80000000)
</dt> <dd>

Laufwerks Administrator

</dd> <dt>

2147483649 (0x80000001)
</dt> <dd>

Drucker Warteschlangen Administrator

</dd> <dt>

2147483650 (0x80000002)
</dt> <dd>

Geräte Administrator

</dd> <dt>

2147483651 (0x80000003)
</dt> <dd>

IPC-Administrator

</dd> </dl> </dd> <dt>

*MaximumAllowed* \[ in, optional\]
</dt> <dd>

Limit für die maximale Anzahl von Benutzern, die diese Ressource gleichzeitig verwenden dürfen.

</dd> <dt>

*Beschreibung* \[ in, optional\]
</dt> <dd>

Eine Beschreibung des Objekts.

</dd> <dt>

*Kennwort* \[ in, optional\]
</dt> <dd>

TBD

</dd> <dt>

*Zugriff* \[ in, optional\]
</dt> <dd>

Optionale eingebettete Instanz einer [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse, die die Sicherheits Beschreibung für die neue Freigabe enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ clustershare**](win32-clustershare.md)
</dt> </dl>

 

