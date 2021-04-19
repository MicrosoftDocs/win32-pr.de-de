---
title: Iwmpcdromcollection getbydrivespecifier-Methode
description: Die getbydrivespecifier-Methode gibt eine iwmpcdrom-Schnittstelle zurück, die einem bestimmten Laufwerk Buchstaben zugeordnet ist.
ms.assetid: 4a550eb1-a37e-43fd-9e08-801c4fd64e68
keywords:
- getbydrivespecifier-Methode, Windows Media Player
- getbydrivespecifier-Methode, Windows Media Player, iwmpcdromcollection-Schnittstelle
- Iwmpcdromcollection-Schnittstelle, Windows Media Player, getbydrivespecifier-Methode
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
ms.openlocfilehash: fe771fc893d4bf43b82dc825a2d33724926e8151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361975"
---
# <a name="iwmpcdromcollectiongetbydrivespecifier-method"></a>Iwmpcdromcollection:: getbydrivespecifier-Methode

Die **getbydrivespecifier** -Methode gibt eine **iwmpcdrom** -Schnittstelle zurück, die einem bestimmten Laufwerk Buchstaben zugeordnet ist.

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

*bstraudrivespecifier* \[ in\]
</dt> <dd>

Eine **System. String** , bei der es sich um den Laufwerk Buchstaben handelt, gefolgt von einem Doppelpunkt (":").

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib. iwmpcdrom** -Schnittstelle.

## <a name="remarks"></a>Bemerkungen

Laufwerk Buchstaben müssen in der Form *x*: angegeben werden, wobei *x* den Laufwerk Buchstaben darstellt.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **getbydrivespecifier** verwendet, um die **iwmpcdrom** -Schnittstelle zu erhalten, die einem Laufwerk Buchstaben entspricht, der vom Benutzer in einem Textfeld bereitgestellt wird. Die **iwmpcdrom. Auswerfen** -Methode wird dann aufgerufen, um das angegebene Laufwerk zu ewerfen. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


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

[**Iwmpcdrom-Schnittstelle (VB und c#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**Iwmpcdrom. eject (VB und c#)**](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md)
</dt> <dt>

[**Iwmpcdromcollection-Schnittstelle (VB und c#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestmediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





