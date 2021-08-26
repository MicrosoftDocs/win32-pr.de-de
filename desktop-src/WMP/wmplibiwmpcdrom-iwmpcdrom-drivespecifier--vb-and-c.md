---
title: IWMPClum driveSpecifier-Eigenschaft
description: Die driveSpecifier-Eigenschaft ruft den Cd- oder DVD-Laufwerkbuchstaben ab.
ms.assetid: 8865232a-08a3-447b-a6d6-2bfda3a689e1
keywords:
- driveSpecifier-Eigenschaft Windows Media Player
- driveSpecifier-Eigenschaft Windows Media Player , IWMPCnutzeroberfläche
- IWMPCaku-Schnittstelle Windows Media Player , driveSpecifier-Eigenschaft
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
ms.openlocfilehash: b555cba0ec694a19a01c040a0369aeb473c6811933d45892cbf3c69ef640b8b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031460"
---
# <a name="iwmpcdromdrivespecifier-property"></a>IWMPClum::d riveSpecifier-Eigenschaft

Die **driveSpecifier-Eigenschaft** ruft den Cd- oder DVD-Laufwerkbuchstaben ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.String driveSpecifier {get; set;}
```


```VB

Public ReadOnly Property driveSpecifier As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.String,die** der Laufwerkbuchstabe ist.

## <a name="remarks"></a>Hinweise

In der Regel können DVD-Laufwerke CD-Medien wiedergeben, cd-Laufwerke können jedoch keine DVD-Medien wiedergeben.

Diese Eigenschaft ruft einen Laufwerkbuchstaben für einen nullbasierten Laufwerkindex innerhalb des Bereichs ab, der mithilfe von **IWMPCcollectionCollection.count** abgerufen wurde. Der abgerufene Wert hat das Format *X*:, wobei *X* den Laufwerkbuchstaben darstellt.

Um den Wert dieser Eigenschaft abzurufen, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **driveSpecifier** verwendet, um eine Zeichenfolge zu erstellen, die eine Liste der verfügbaren CD- und DVD-Laufwerke enthält und diese Zeichenfolge in einem Meldungsfeld anzeigt. Das **AxWMPLib.AxWindowsMediaPlayer-Objekt** wird durch die Variable player dargestellt.


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
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPCorpora-Schnittstelle (VB und C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPCcollectionCollection.count (VB und C#)**](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





