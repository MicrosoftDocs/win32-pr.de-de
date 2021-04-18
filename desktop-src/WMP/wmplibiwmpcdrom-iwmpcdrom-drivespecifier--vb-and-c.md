---
title: Iwmpcdrom-drivespecifier (Eigenschaft)
description: Mit der drivespecifier-Eigenschaft wird der CD-oder DVD-Laufwerk Buchstabe abgerufen.
ms.assetid: 8865232a-08a3-447b-a6d6-2bfda3a689e1
keywords:
- drivespecifier-Eigenschaften Fenster Media Player
- drivespecifier-Eigenschaft, Windows Media Player, iwmpcdrom-Schnittstelle
- Iwmpcdrom-Schnittstelle, Windows Media Player, drivespecifier (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPCdrom.driveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a6c439523d90824da708700d48274f5a2e5ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360898"
---
# <a name="iwmpcdromdrivespecifier-property"></a>Iwmpcdrom::d rivespecifier (Eigenschaft)

Mit der **drivespecifier** -Eigenschaft wird der CD-oder DVD-Laufwerk Buchstabe abgerufen.

## <a name="syntax"></a>Syntax


```CSharp
public System.String driveSpecifier {get; set;}
```


```VB

Public ReadOnly Property driveSpecifier As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. String** -Wert, der der Laufwerk Buchstabe ist.

## <a name="remarks"></a>Bemerkungen

In der Regel können DVD-Laufwerke CD-Medien wiedergeben, während CD-Laufwerke keine DVD-Medien abspielen können.

Diese Eigenschaft ruft einen Laufwerk Buchstaben für einen NULL basierten Laufwerks Index innerhalb des Bereichs ab, der mithilfe von **iwmpcdromcollection. count** abgerufen wird. Der abgerufene Wert hat die Form *x*:, wobei *X* den Laufwerk Buchstaben darstellt.

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **drivespecifier** verwendet, um eine Zeichenfolge zu erstellen, die eine Liste der verfügbaren CD-und DVD-Laufwerke enthält und diese Zeichenfolge in einem Meldungs Feld anzeigt. Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.


```CSharp
// String that will contain the list of drive specifiers.
string MyDriveSpecifiers = "Drive letters found:  ";

// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives. 
for (int i = 0; i < numDrives; i++)
{
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier;
    MyDriveSpecifiers += " ";
}

// Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers);
```


```VB

'  String that will contain the list of drive specifiers.
Dim MyDriveSpecifiers As String = &quot;Drive letters found:  &quot;

&#39;  Store the number of available drives.
Dim numDrives = player.cdromCollection.count

&#39;  Loop through the available drives. 
For i As Integer = 0 To (numDrives - 1)
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier
    MyDriveSpecifiers += &quot; &quot;
Next i

&#39;  Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers)
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

[**Iwmpcdromcollection. Count (VB und c#)**](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestmediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





