---
title: IWMPCcollection getByDriveSpecifier-Methode
description: Die getByDriveSpecifier-Methode gibt eine IWMPCome-Schnittstelle zurück, die einem bestimmten Laufwerkbuchstaben zugeordnet ist.
ms.assetid: 4a550eb1-a37e-43fd-9e08-801c4fd64e68
keywords:
- getByDriveSpecifier-Windows Media Player
- getByDriveSpecifier-Methode Windows Media Player , IWMPCcollection-Schnittstelle
- IWMPCcollection-Schnittstelle Windows Media Player , getByDriveSpecifier-Methode
topic_type:
- apiref
api_name:
- IWMPCdromCollection.getByDriveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9937694234fe7e46fe9b98d83357da19abf18f8d14e83794587f6f2050b0019b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116218"
---
# <a name="iwmpcdromcollectiongetbydrivespecifier-method"></a>IWMPCcollection::getByDriveSpecifier-Methode

Die **getByDriveSpecifier-Methode** gibt eine **IWMPCome-Schnittstelle zurück,** die einem bestimmten Laufwerkbuchstaben zugeordnet ist.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPCdrom getByDriveSpecifier(
  System.String bstrDriveSpecifier
);
```


```VB

Public Function getByDriveSpecifier( _
  ByVal bstrDriveSpecifier As System.String _
) As IWMPCdrom
Implements IWMPCdromCollection.getByDriveSpecifier
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrDriveSpecifier* \[ In\]
</dt> <dd>

Eine **System.String,** bei der es sich um den Laufwerkbuchstaben gefolgt von einem Doppelpunkt (":") handelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib.IWMPCface-Schnittstelle.**

## <a name="remarks"></a>Hinweise

Laufwerkbuchstaben müssen in der Form *X*: angegeben werden, wobei *X* den Laufwerkbuchstaben darstellt.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **getByDriveSpecifier** verwendet, um die **IWMPCifier-Schnittstelle** zu erhalten, die einem Laufwerkbuchstaben entspricht, der vom Benutzer in einem Textfeld bereitgestellt wird. Die **IWMPC festplatten.eject-Methode** wird dann aufgerufen, um das angegebene Laufwerk auswerfen. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


```CSharp
// Store the drive letter provided by the user.
string driveLetter = myText.Text;

// Append a colon to the drive letter to create a valid drive specifier.
driveLetter += ":";

// Get an IWMPCdrom interface for the drive.
WMPLib.IWMPCdrom drive = player.cdromCollection.getByDriveSpecifier(driveLetter);

// Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject();
```


```VB

' Store the drive letter provided by the user.
Dim driveLetter As String = myText.Text

&#39; Append a colon to the drive letter to create a valid drive specifier.
driveLetter += &quot;:&quot;

&#39; Get an IWMPCdrom interface for the drive.
Dim drive As WMPLib.IWMPCdrom = player.cdromCollection.getByDriveSpecifier(driveLetter)

&#39; Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject()
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPCwertschnittstelle (VB und C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPC datenträger.eject (VB und C#)**](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md)
</dt> <dt>

[**IWMPCcollection-Schnittstelle (VB und C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





