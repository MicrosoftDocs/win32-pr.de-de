---
title: Zgstoreconsentmsg-Methode der Win32_TSGatewayServerSettings-Klasse
description: Aktualisiert die Zustimmungs Nachricht für den Gatewayserver.
ms.assetid: b3146d87-95af-4b6b-8c02-5ac4748fbe98
ms.tgt_platform: multiple
keywords:
- Zgstoreconsentmsg-Methode Remotedesktopdienste
- Methode Remotedesktopdienste der Methode "zgstoreconsentmsg", Win32_TSGatewayServerSettings Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, Methode "zgstoreconsentmsg"
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreConsentMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907097739d21e1523aca3b719cdb5f18b6f3fa30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477091"
---
# <a name="tsgstoreconsentmsg-method-of-the-win32_tsgatewayserversettings-class"></a>Zgstoreconsentmsg-Methode der Win32-Klasse "t- \_ gatewayserversettings"

Aktualisiert die Zustimmungs Nachricht für den Gatewayserver.

## <a name="syntax"></a>Syntax


```mof
uint32 TSGStoreConsentMsg(
  [in] string TSGConMsgText
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

GS-Verbindungs *Text* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Der Zustimmungs Meldungs Text.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                        |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>"T-Gateway. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Datei- \_ gatewayserversettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

